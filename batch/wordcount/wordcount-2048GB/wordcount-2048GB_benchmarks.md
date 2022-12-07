# Wordcount Benchmarks: 2048 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 2004.82 GB (grep)
  2. 2004.76 GB (used in the data processing benchmarks below)
  3. 2004.72 GB (grep-extra)

- Generation Time:
  1. 11855 seconds (grep)
  2. 11429 seconds
  3. 11436 seconds (grep-extra)

- Loading Time (HDFS):
  1. 2671 seconds (grep)
  2. 2667 seconds
  3. 2659 seconds (grep-extra)

- Loading Time (Unicage):
  1. 3248 seconds (grep)
  2. 3081 seconds
  3. 3079 seconds (grep-extra)


### ***Hadoop***

- Implementation: [WordCount.java](../../../../../workloads/batch/wordcount/javaWordcount/Wordcount/src/main/java/WordCount.java)

- Output Hash:
  1. a1543830a73679f41d6b457305eb5b3d
  2. a1543830a73679f41d6b457305eb5b3d
  3. a1543830a73679f41d6b457305eb5b3d

- Execution Time: 
  1. 33616 seconds
  2. 33582 seconds
  3. 33635 seconds

- Data Processed Per Second:
  1. 0.06092336982389338410 GB/s
  2. 0.06098505151569293073 GB/s
  3. 0.06088895495763341757 GB/s


### ***Spark***

- Implementation: [Wordcount.scala (fixed)](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala)

- Output Hash:
  1. a1543830a73679f41d6b457305eb5b3d
  2. a1543830a73679f41d6b457305eb5b3d
  3. a1543830a73679f41d6b457305eb5b3d

- Execution Time: 
  1. 6720 seconds
  2. 6724 seconds
  3. 6730 seconds

- Data Processed Per Second:
  1. 0.30476190476190476190 GB/s
  2. 0.30458060678167757287 GB/s
  3. 0.30430906389301634472 GB/s


### ***Unicage***

- Implementation: [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh)

- Output Hash:
  1. a1543830a73679f41d6b457305eb5b3d
  2. a1543830a73679f41d6b457305eb5b3d
  3. a1543830a73679f41d6b457305eb5b3d

- Execution Time: 
  1. 10413 seconds
  2. 10349 seconds
  3. 10164 seconds

- Data Processed Per Second:
  1. 0.19667723038509555363 GB/s
  2. 0.19789351628176635423 GB/s
  3. 0.20149547422274695001 GB/s


---
## Special Considerations:

- Hadoop and Spark were in agreement, but not the Unicage implementation. The output of the Unicage implementation had an "healthy" structure. ~~The results reported in this document reflect 3 runs of [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh)~~. the problem was a buffer overflow in both the implementations of Spark and Hadoop, and it was fixed by changing the counter from *int* to *long* in both implementations.

---
## Conclusions:

TODO

