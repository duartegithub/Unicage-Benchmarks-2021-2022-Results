## Sort Benchmarks: 512 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 501.25 GB (grep)
  2. TODO
  3. TODO

- Generation Time:
  1. 4281 seconds
  2. TODO
  3. TODO

- Loading Time (HDFS):
  1. 886 seconds
  2. TODO
  3. TODO

- Loading Time (Unicage):
  1. 754 seconds
  2. TODO
  3. TODO


### ***Hadoop***

- Output Hash:
  1. dfc02e200a9a091692f2e7543a0fabe7
  2. TODO
  3. TODO

- Execution Time: 
  1. 134774 seconds
  2. TODO
  3. TODO

- Data Processed Per Second:
  1. 0.00379895232018045023 GB/s
  2. TODO
  3. TODO


### ***Spark***

- Implementation: [Sort.scala](../../../../../workloads/batch/sort/scalaSort/src/main/scala/Sort.scala)

- Output Hash:
  1. dfc02e200a9a091692f2e7543a0fabe7
  2. dfc02e200a9a091692f2e7543a0fabe7
  3. dfc02e200a9a091692f2e7543a0fabe7

- Execution Time: 
  1. 20350 seconds
  2. 20091 seconds
  3. 20001 seconds

- Data Processed Per Second: 
  1. 0.02515970515970515970 GB/s
  2. 0.02548404758349509730 GB/s
  3. 0.02559872006399680015 GB/s


### ***Unicage***

- Implementation: [boaSort-fixed.sh](../../../../../workloads/batch/sort/bashSort/boaSort/boaSort-fixed.sh)

- Output Hash:
  1. a552948245fbf401c381191f88fc16bc
  2. df58d2a8e36e10a3ae52d7cde1a6b536
  3. a6515436cea5d31ef1364234b09bf78d

- Execution Time: 
  1. 14057 seconds
  2. 14256 seconds
  3. 14023 seconds

- Data Processed Per Second:
  1. 0.03642313438144696592 GB/s
  2. 0.03591470258136924803 GB/s
  3. 0.03651144548242173571 GB/s


---
## Special Considerations:

- Against what was predicted, Unicage was not able to finish Sort-512GB due to an error. This error is present in the [nohup.out-error](./unicage-result/nohup.out-error) logfile. The first half of the script, that sorts each individual file in the unicageworkers seems to be working correctly. However the second half, when the distr-dmerge command is used to merge all individual files in a single output file in the unicageleader, fails with the following errors coming from each unicageworker:

  > root@unicageleader:~# distr-dmerge ~/unicageworkers key=1 ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.* > ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/output \
  > Error(4271)[dmerge] : file '/root/datav/outputs/batch/sort/sort-512GB-results/ unicage-result/sort.997' not found. \
  > Error(4271)[dmerge] : file '/root/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.997' not found. \
  > Error(4271)[dmerge] : file '/root/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.997' not found. \
  > Error(4271)[dmerge] : file '/root/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.997' not found. \
  > Error(4271)[dmerge] : file '/root/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.997' not found.

  This file (.../unicage-result/sort.997) exists in every unicageworker, and running the same command, without the wildcard (*), works correctly:

  > root@unicageleader:~# distr-dmerge ~/unicageworkers key=1 ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.997 > ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/output \
  > (exits normally and produces a correct output)

  The same command with a more restrictive wildcards also work correctly:

  > root@unicageleader:~# distr-dmerge ~/unicageworkers key=1 ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.99* > ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/output \
  > (exits normally and produces a correct output)

  > root@unicageleader:~# distr-dmerge ~/unicageworkers key=1 ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/sort.9* > ~/datav/outputs/batch/sort/sort-512GB-results/unicage-result/output \
  > (exits normally and produces a correct output)

  A simple test shows that dmerge stops working when the number of files encompassed by the wildcard is larger than 1021:

  > root@unicageleader:~# for i in {1..1021}; do touch ./testing/input/$i; echo $RANDOM > ./testing/input/$i; done \
  > root@unicageleader:~# dmerge key=1 ./testing/input/* > ./testing/output/merged \
  > root@unicageleader:~# cat ./testing/output/merged \
  > (1 column, 1021 sorted rows)

  > root@unicageleader:~# rm ./testing/input/* \
  > root@unicageleader:~# for i in {1..1022}; do touch ./testing/input/$i; echo $RANDOM > ./testing/input/$i; done \
  > root@unicageleader:~# dmerge key=1 ./testing/input/* > ./testing/output/merged \
  > Error(4271)[dmerge] : file './testing/input/999' not found.

  To address this problem, a fix that introduces the intermediate step of dividing the intermediate files in batches of 1000 was implemented in the Unicage implementation of sort. With this in mind, the results reported in this document reflect 3 runs of [boaSort-fixed.sh](../../../../../workloads/batch/sort/bashSort/boaSort/boaSort-fixed.sh) instead of [boaSort.sh](../../../../../workloads/batch/sort/bashSort/boaSort/boaSort.sh). The output of this fixed implementation was incoherent between runs and did not match that of Spark. This incoherence in outputs indicates the Unicage implementation did not handle the 512 GB input properly.


---
## Conclusions: