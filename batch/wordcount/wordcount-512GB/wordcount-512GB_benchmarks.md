# Wordcount Benchmarks: 512 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 501.34 GB (grep)
  2. 501.13 GB (used in the data processing benchmarks below)
  3. 501.20 GB (grep-extra)

- Generation Time:
  1. 2961 seconds (grep)
  2. 2858 seconds
  3. 2867 seconds (grep-extra)

- Loading Time (HDFS):
  1. 664 seconds (grep)
  2. 663 seconds
  3. 664 seconds (grep-extra)

- Loading Time (Unicage):
  1. 736 seconds (grep)
  2. 739 seconds
  3. 743 seconds (grep_extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/wordcount/javaWordcount/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 1323e698a454044638ca51722433a58c
  2. 1323e698a454044638ca51722433a58c
  3. 1323e698a454044638ca51722433a58c

- Execution Time: 
  1. 8615 seconds
  2. 8422 seconds
  3. 8405 seconds

- Data Processed Per Second: 
  1. 0.05943122460824143934 GB/s
  2. 0.06079316076941344098 GB/s
  3. 0.06091612135633551457 GB/s


### ***Spark***

- Implementation: [Wordcount.scala](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala%20(buffer%20overflow))

- Output Hash:
  1. 1323e698a454044638ca51722433a58c
  2. 1323e698a454044638ca51722433a58c
  3. 1323e698a454044638ca51722433a58c

- Execution Time: 
  1. 1740 seconds
  2. 1530 seconds
  3. 1486 seconds

- Data Processed Per Second:
  1. 0.29425287356321839080 GB/s
  2. 0.33464052287581699346 GB/s
  3. 0.34454912516823687752 GB/s


### ***Unicage***

- Implementation: [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh)

- Output Hash:
  1. 1323e698a454044638ca51722433a58c
  2. 1323e698a454044638ca51722433a58c
  3. 1323e698a454044638ca51722433a58c

- Execution Time: 
  1. 2532 seconds
  2. 2530 seconds
  3. 2531 seconds

- Data Processed Per Second:
  1. 0.20221169036334913112 GB/s
  2. 0.20237154150197628458 GB/s
  3. 0.20229158435401027261 GB/s


---
## Special Considerations:

- Against what was predicted, Unicage was not able to finish Wordcount-512GB due to an error. This error is present in the [nohup.out-error](./unicage-result/nohup.out-error) logfile. The first part of the first half of the script, that counts the number of words in each individual file in the unicageworkers seems to be working correctly. However the second part of the first half of the script when the dmerge command is used to merge all individual files in a single split output file in each nicageworker, fails with the following errors coming from each unicageworker:

  > root@unicageworker1:~# dmerge key=1 ~/datav/outputs/batch/wordcount/wordcount-512GB-results/unicage-result/counts/* | sm2 1 1 2 2 > ~/datav/outputs/batch/wordcount/wordcount-512GB-results/unicage-result/split \
  > Error(4271)[dmerge] : file '/root/datav/outputs/batch/wordcount/wordcount-512GB-results/unicage-result/counts/lda_wiki1w_9_producer1-counts' not found. 

  **EDIT:** This file (.../unicage-result/lda_wiki1w_9_producer1-counts) exists in each unicageworker. This is believed to be the same bug that prevented Sort-512GB from working. This bug is well documented in [this document](../../sort/sort-512GB/sort-512GB_benchmarks.md).

  **EDIT:** To address this problem, just like in the Sort-512GB case, a fix that introduces the intermediate step of dividing the intermediate files in batches of 1000 was implemented. With this in mind, the results reported in this document reflect 3 runs of [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh) instead of [boaWordcount.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount.sh). There was no performance impact.


---
## Conclusions:

TODO