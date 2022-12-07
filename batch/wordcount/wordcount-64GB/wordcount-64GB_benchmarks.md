# Wordcount Benchmarks: 64 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 62.69 GB (grep)
  2. 62.68 GB (used in the data processing benchmarks below)
  3. 62.66 GB (grep-extra)

- Generation Time:
  1. 382 seconds (grep)
  2. 371 seconds 
  3. 363 seconds (grep-extra)

- Loading Time (HDFS):
  1. 72 seconds (grep)
  2. 65 seconds 
  3. 66 seconds (grep-extra)

- Loading Time (Unicage):
  1. 74 seconds (grep)
  2. 83 seconds 
  3. 75 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/wordcount/javaWordcount/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. c459e4ff053a84b0ea9f0f9dba75a35e
  2. c459e4ff053a84b0ea9f0f9dba75a35e
  3. c459e4ff053a84b0ea9f0f9dba75a35e

- Execution Time: 
  1. 1094 seconds
  2. 1074 seconds
  3. 1075 seconds

- Data Processed Per Second:
  1. 0.05850091407678244972 GB/s
  2. 0.05959031657355679702 GB/s
  3. 0.05953488372093023255 GB/s


### ***Spark***

- Implementation: [Wordcount.scala](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala%20(buffer%20overflow))

- Output Hash:
  1. c459e4ff053a84b0ea9f0f9dba75a35e
  2. c459e4ff053a84b0ea9f0f9dba75a35e
  3. c459e4ff053a84b0ea9f0f9dba75a35e

- Execution Time: 
  1. 214 seconds
  2. 201 seconds
  3. 199 seconds

- Data Processed Per Second:
  1. 0.29906542056074766355 GB/s
  2. 0.31840796019900497512 GB/s
  3. 0.32160804020100502512 GB/s


### ***Unicage***

- Implementation: [boaWordcount.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount.sh)

- Output Hash:
  1. c459e4ff053a84b0ea9f0f9dba75a35e
  2. c459e4ff053a84b0ea9f0f9dba75a35e
  3. c459e4ff053a84b0ea9f0f9dba75a35e

- Execution Time: 
  1. 315 seconds
  2. 315 seconds
  3. 314 seconds

- Data Processed Per Second:
  1. 0.20317460317460317460 GB/s
  2. 0.20317460317460317460 GB/s
  3. 0.20382165605095541401 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO