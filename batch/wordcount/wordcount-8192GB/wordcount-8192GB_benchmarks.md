# Wordcount Benchmarks: 8192 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 8019.19 GB (grep)
  2. 8018.54 GB (used in the data processing benchmarks below)
  3. 8018.60 GB (grep-extra)

- Generation Time:
  1. 47573 seconds (grep)
  2. 45694 seconds 
  3. 45618 seconds (grep-extra)

- Loading Time (HDFS):
  1. 10780 seconds (grep)
  2. 10704 seconds
  3. 10916 seconds (grep-extra)

- Loading Time (Unicage):
  1. 14843 seconds (grep)
  2. 12705 seconds
  3. 12632 seconds (grep-extra)


### ***Hadoop***

- Output Hash:
  1. 6c7bd2e69714c0a127ea560c470eb58a
  2. TODO
  3. TODO

- Execution Time: 
  1. 135883 seconds
  2. TODO
  3. TODO

- Data Processed Per Second:
  1. 0.06028715880573728869 GB/s
  2. TODO
  3. TODO


### ***Spark***

- Implementation: [Wordcount.scala (fixed)](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala)

- Output Hash:
  1. Out of Memory
  2. Out of Memory
  3. TODO

- Execution Time: 
  1. Out of Memory
  2. Out of Memory
  3. TODO

- Data Processed Per Second:
  1. Out of Memory
  2. Out of Memory
  3. TODO


### ***Unicage***

- Implementation: [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh)

- Output Hash:
  1. 22803360815d8fed448c709fe7bcd18c (6c7bd2e69714c0a127ea560c470eb58a)
  2. 22803360815d8fed448c709fe7bcd18c
  3. 22803360815d8fed448c709fe7bcd18c

- Execution Time: 
  1. 41418 seconds
  2. 41366 seconds
  3. 41442 seconds

- Data Processed Per Second:
  1. 0.19778840117823168670 GB/s
  2. 0.19803703524633757191 GB/s
  3. 0.19767385743931277447 GB/s


---
## Special Considerations:

- Spark did not finish wordcount on a 8192 GB input data-set due to multiple OutOfMemoryError Java exceptions being thrown. 

  The [nohup.out-out-of-memory](./spark-result/nohup.out-out-of-memory) file logs this error (the process had to be forcefully terminated after the error in the second run).

- The benchmark of Unicage was verified with Hadoop. However, by the time this was done, the previous data-set used in the benchmark was no longer in the cluster, so a wordcount run was recreated with a new data-set with Unicage (logged in [nohup.out-verified-with-hadoop](./unicage-result/nohup.out-verified-with-hadoop)), and a single run of Hadoop was performed to verify the correctness of the Unicage solution (logged in [hadoop-result/nohup.out-run1](./hadoop-result/nohup.out-run1)).


---
## Conclusions:

TODO