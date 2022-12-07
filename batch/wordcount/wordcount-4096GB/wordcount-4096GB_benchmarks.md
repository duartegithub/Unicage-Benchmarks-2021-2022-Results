# Wordcount Benchmarks: 4096 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 4009.08 GB (grep)
  2. 4008.87 GB (used in the data processing benchmarks below)
  3. 4008.95 GB (grep-extra)

- Generation Time:
  1. 23620 seconds (grep)
  2. 22811 seconds
  3. 22893 seconds (grep-extra)

- Loading Time (HDFS):
  1. 5370 seconds (grep)
  2. 5352 seconds
  3. 5367 seconds (grep-extra)

- Loading Time (Unicage):
  1. 6272 seconds (grep)
  2. 6202 seconds
  3. 6195 seconds (grep-extra)


### ***Hadoop***

- Implementation: [WordCount.java](../../../../../workloads/batch/wordcount/javaWordcount/Wordcount/src/main/java/WordCount.java)

- Output Hash:
  1. b44b693659df34c736806aac2de411c5
  2. b44b693659df34c736806aac2de411c5
  3. b44b693659df34c736806aac2de411c5

- Execution Time: 
  1. 69034 seconds
  2. 67654 seconds
  3. 67410 seconds

- Data Processed Per Second: 
  1. 0.05933308224932641886 GB/s
  2. 0.06054335294291542259 GB/s
  3. 0.06076249814567571576 GB/s


### ***Spark***

- Implementation: [Wordcount.scala (fixed)](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala)

- Output Hash:
  1. b44b693659df34c736806aac2de411c5
  2. b44b693659df34c736806aac2de411c5
  3. b44b693659df34c736806aac2de411c5

- Execution Time: 
  1. 15297 seconds
  2. 14494 seconds
  3. 14551 seconds

- Data Processed Per Second:
  1. 0.26776492122638425835 GB/s
  2. 0.28259969642610735476 GB/s
  3. 0.28149268091540100336 GB/s


### ***Unicage***

- Implementation: [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh)

- Output Hash:
  1. b44b693659df34c736806aac2de411c5
  2. b44b693659df34c736806aac2de411c5
  3. b44b693659df34c736806aac2de411c5

- Execution Time: 
  1. 20692 seconds
  2. 20613 seconds
  3. 20624 seconds

- Data Processed Per Second:
  1. 0.19855543167385719133 GB/s
  2. 0.19870955222432445544 GB/s
  3. 0.19860356865787432117 GB/s


---
## Special Considerations:

- Spark's nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO