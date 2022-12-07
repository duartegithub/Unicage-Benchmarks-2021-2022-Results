# Wordcount Benchmarks: 1024 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 1002.10 GB (grep)
  2. 1002.19 GB (used in the data processing benchmarks below)
  3. 1002.26 GB (grep-extra)

- Generation Time:
  1. 5884 seconds (grep)
  2. 5711 seconds
  3. 5723 seconds (grep-extra)

- Loading Time (HDFS):
  1. 1340 seconds (grep)
  2. 1343 seconds
  3. 1341 seconds (grep-extra)

- Loading Time (Unicage):
  1. 1521 seconds (grep)
  2. 1525 seconds
  3. 1519 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/wordcount/javaWordcount/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 893053c38e453d7cab0d6b9f14207dc8
  2. 893053c38e453d7cab0d6b9f14207dc8
  3. 893053c38e453d7cab0d6b9f14207dc8

- Execution Time: 
  1. 17054 seconds
  2. 16948 seconds
  3. 17066 seconds

- Data Processed Per Second: 
  1. 0.06004456432508502404 GB/s
  2. 0.06042010856738258201 GB/s
  3. 0.06000234384155631079 GB/s


### ***Spark***

- Implementation: [Wordcount.scala](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala%20(buffer%20overflow))

- Output Hash:
  1. 893053c38e453d7cab0d6b9f14207dc8
  2. 893053c38e453d7cab0d6b9f14207dc8
  3. 893053c38e453d7cab0d6b9f14207dc8

- Execution Time: 
  1. 3015 seconds
  2. 2958 seconds
  3. 2990 seconds

- Data Processed Per Second:
  1. 0.33963515754560530679 GB/s
  2. 0.34617985125084516565 GB/s
  3. 0.34247491638795986622 GB/s


### ***Unicage***

- Implementation: [boaWordcount-fixed.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount-fixed.sh)

- Output Hash:
  1. 893053c38e453d7cab0d6b9f14207dc8
  2. 893053c38e453d7cab0d6b9f14207dc8
  3. 893053c38e453d7cab0d6b9f14207dc8

- Execution Time: 
  1. 5064 seconds
  2. 5071 seconds
  3. 5064 seconds

- Data Processed Per Second: 
  1. 0.20221169036334913112 GB/s
  2. 0.20193255768093078288 GB/s
  3. 0.20221169036334913112 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO