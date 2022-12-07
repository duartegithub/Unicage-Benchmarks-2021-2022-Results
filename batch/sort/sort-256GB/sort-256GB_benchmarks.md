# Sort Benchmarks: 256 GB

---
## Benchmark Results:

- Generation Time:
  1. 2125 seconds
  2. TODO
  3. TODO

- Loading Time (HDFS):
  1. 319 seconds
  2. TODO
  3. TODO

- Loading Time (Unicage):
  1. 378 seconds
  2. TODO
  3. TODO


### ***Hadoop***

- Implementation: [Sort.java](../../../../../workloads/batch/sort/javaSort/Sort/src/main/java/Sort.java)

- Output Hash:
  1. 9f01a9e4307c1e0aeb30fd1afd3c2ef4
  2. 9f01a9e4307c1e0aeb30fd1afd3c2ef4
  3. 9f01a9e4307c1e0aeb30fd1afd3c2ef4

- Execution Time: 
  1. 62110 seconds
  2. 62546 seconds
  3. 63077 seconds

- Data Processed Per Second:
  1. 0.00412171952986636612 GB/s
  2. 0.00409298756115498992 GB/s
  3. 0.00405853163593702934 GB/s


### ***Spark***

- Implementation: [Sort.scala](../../../../../workloads/batch/sort/scalaSort/src/main/scala/Sort.scala)

- Output Hash:
  1. 9f01a9e4307c1e0aeb30fd1afd3c2ef4
  2. 9f01a9e4307c1e0aeb30fd1afd3c2ef4
  3. 9f01a9e4307c1e0aeb30fd1afd3c2ef4

- Execution Time: 
  1. 10119 seconds
  2. 10045 seconds
  3. 10138 seconds

- Data Processed Per Second:
  1. 0.02529894258325921533 GB/s
  2. 0.02548531607765057242 GB/s
  3. 0.02525152890116393766 GB/s


### ***Unicage***

- Implementation: [boaSort.sh](../../../../../workloads/batch/sort/bashSort/boaSort/boaSort.sh)

- Output Hash:
  1. 9f01a9e4307c1e0aeb30fd1afd3c2ef4
  2. 9f01a9e4307c1e0aeb30fd1afd3c2ef4
  3. 9f01a9e4307c1e0aeb30fd1afd3c2ef4

- Execution Time: 
  1. 6439 seconds
  2. 6436 seconds
  3. 6463 seconds

- Data Processed Per Second:
  1. 0.03975772635502407206 GB/s
  2. 0.03977625854568054692 GB/s
  3. 0.03961008819433699520 GB/s


---
## Special Considerations:

TODO

---
## Conclusions:

TODO