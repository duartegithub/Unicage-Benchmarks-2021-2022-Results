# Sort Benchmarks: 64 GB

---
## Benchmark Results:

- Generation Time:
  1. 466 seconds
  2. TODO
  3. TODO

- Loading Time (HDFS):
  1. 68 seconds
  2. TODO
  3. TODO

- Loading Time (Unicage):
  1. 82 seconds
  2. TODO
  3. TODO


### ***Hadoop***

- Implementation: [Sort.java](../../../../../workloads/batch/sort/javaSort/Sort/src/main/java/Sort.java)

- Output Hash:
  1. 1980a08b6b20e0de202ebfd419762f2a
  2. 1980a08b6b20e0de202ebfd419762f2a
  3. 1980a08b6b20e0de202ebfd419762f2a

- Execution Time: 
  1. 13028 seconds
  2. 13014 seconds
  3. 13089 seconds

- Data Processed Per Second:
  1. 0.00491249616211237334 GB/s
  2. 0.00491778085139080989 GB/s
  3. 0.00488960195584078233 GB/s


### ***Spark***

- Implementation: [Sort.scala](../../../../../workloads/batch/sort/scalaSort/src/main/scala/Sort.scala)

- Output Hash:
  1. 1980a08b6b20e0de202ebfd419762f2a
  2. 1980a08b6b20e0de202ebfd419762f2a
  3. 1980a08b6b20e0de202ebfd419762f2a

- Execution Time: 
  1. 2758 seconds
  2. 2750 seconds
  3. 2760 seconds

- Data Processed Per Second:
  1. 0.02320522117476432197 GB/s
  2. 0.02327272727272727272 GB/s
  3. 0.02318840579710144927 GB/s


### ***Unicage***

- Implementation: [boaSort.sh](../../../../../workloads/batch/sort/bashSort/boaSort/boaSort.sh)

- Output Hash:
  1. 1980a08b6b20e0de202ebfd419762f2a
  2. 1980a08b6b20e0de202ebfd419762f2a
  3. 1980a08b6b20e0de202ebfd419762f2a

- Execution Time: 
  1. 1560 seconds
  2. 1541 seconds
  3. 1554 seconds

- Data Processed Per Second:
  1. 0.04102564102564102564 GB/s
  2. 0.04153147306943543153 GB/s
  3. 0.04118404118404118404 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO