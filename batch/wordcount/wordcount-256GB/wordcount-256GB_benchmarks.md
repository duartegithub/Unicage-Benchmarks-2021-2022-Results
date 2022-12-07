# Wordcount Benchmarks: 256 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 250.63 GB (grep)
  2. 250.57 GB (used in the data processing benchmarks below)
  3. 250.79 GB (grep-extra)

- Generation Time:
  1. 1483 seconds (grep)
  2. 1430 seconds
  3. 1436 seconds (grep-extra)

- Loading Time (HDFS):
  1. 316 seconds (grep)
  2. 321 seconds
  3. 316 seconds (grep-extra)

- Loading Time (Unicage):
  1. 343 seconds (grep)
  2. 336 seconds
  3. 347 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/wordcount/javaWordcount/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 3af79d916eb5f4fc79592fd8b428421c
  2. 3af79d916eb5f4fc79592fd8b428421c
  3. 3af79d916eb5f4fc79592fd8b428421c

- Execution Time: 
  1. 4316 seconds
  2. 4243 seconds
  3. 4238 seconds

- Data Processed Per Second: 
  1. 0.05931417979610750695 GB/s
  2. 0.06033466886636813575 GB/s
  3. 0.06040585181689476168 GB/s


### ***Spark***

- Implementation: [Wordcount.scala](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala%20(buffer%20overflow))

- Output Hash:
  1. 3af79d916eb5f4fc79592fd8b428421c
  2. 3af79d916eb5f4fc79592fd8b428421c
  3. 3af79d916eb5f4fc79592fd8b428421c

- Execution Time: 
  1. 726 seconds
  2. 713 seconds
  3. 733 seconds

- Data Processed Per Second:
  1. 0.35261707988980716253 GB/s
  2. 0.35904628330995792426 GB/s
  3. 0.34924965893587994542 GB/s


### ***Unicage***

- Implementation: [boaWordcount.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount.sh)

- Output Hash:
  1. 3af79d916eb5f4fc79592fd8b428421c
  2. 3af79d916eb5f4fc79592fd8b428421c
  3. 3af79d916eb5f4fc79592fd8b428421c

- Execution Time: 
  1. 1274 seconds
  2. 1275 seconds
  3. 1273 seconds

- Data Processed Per Second:
  1. 0.20094191522762951334 GB/s
  2. 0.20078431372549019607 GB/s
  3. 0.20109976433621366849 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO