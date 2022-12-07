# Grep Benchmarks: 128 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 125.23 GB (used in the data processing benchmarks below)
  2. 125.24 GB (wordcount)
  3. 125.28 GB (grep-extra)

- Generation Time:
  1. 768 seconds
  2. 736 seconds (wordcount)
  3. 737 seconds (grep-extra)

- Loading Time (HDFS):
  1. 137 seconds
  2. 144 seconds (wordcount)
  3. 134 seconds (grep-extra)

- Loading Time (Unicage):
  1. 150 seconds
  2. 150 seconds (wordcount)
  3. 162 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 417090f7e2b3343ec1aed18a7769afc6
  2. 417090f7e2b3343ec1aed18a7769afc6
  3. 417090f7e2b3343ec1aed18a7769afc6

- Execution Time: 
  1. 396 seconds
  2. 391 seconds
  3. 389 seconds

- Data Processed Per Second: 
  1. 0.32323232323232323232 GB/s
  2. 0.32736572890025575447 GB/s
  3. 0.32904884318766066838 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. 417090f7e2b3343ec1aed18a7769afc6
  2. 417090f7e2b3343ec1aed18a7769afc6
  3. 417090f7e2b3343ec1aed18a7769afc6

- Execution Time: 
  1. 190 seconds
  2. 190 seconds
  3. 191 seconds

- Data Processed Per Second: 
  1. 0.67368421052631578947 GB/s
  2. 0.67368421052631578947 GB/s
  3. 0.67015706806282722513 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. 417090f7e2b3343ec1aed18a7769afc6
  2. 417090f7e2b3343ec1aed18a7769afc6
  3. 417090f7e2b3343ec1aed18a7769afc6

- Execution Time: 
  1. 137 seconds
  2. 136 seconds
  3. 136 seconds

- Data Processed Per Second: 
  1. 0.93430656934306569343 GB/s
  2. 0.94117647058823529411 GB/s
  3. 0.94117647058823529411 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO