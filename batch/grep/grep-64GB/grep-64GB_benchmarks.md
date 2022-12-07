# Grep Benchmarks: 64 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 62.69 GB (used in the data processing benchmarks below)
  2. 62.68 GB (wordcount)
  3. 62.66 GB (grep-extra)

- Generation Time:
  1. 382 seconds
  2. 371 seconds (wordcount)
  3. 363 seconds (grep-extra)

- Loading Time (HDFS):
  1. 72 seconds
  2. 65 seconds (wordcount)
  3. 66 seconds (grep-extra)

- Loading Time (Unicage):
  1. 74 seconds
  2. 83 seconds (wordcount)
  3. 75 seconds (grep-extra)


### ***Hadoop*** 

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 6b111dadbcdabed8adf4b1832a06f6fc
  2. 6b111dadbcdabed8adf4b1832a06f6fc
  3. 6b111dadbcdabed8adf4b1832a06f6fc

- Execution Time: 
  1. 212 seconds
  2. 210 seconds
  3. 211 seconds

- Data Processed Per Second: 
  1. 0.30188679245283018867 GB/s
  2. 0.30476190476190476190 GB/s
  3. 0.30331753554502369668 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. 6b111dadbcdabed8adf4b1832a06f6fc
  2. 6b111dadbcdabed8adf4b1832a06f6fc
  3. 6b111dadbcdabed8adf4b1832a06f6fc

- Execution Time: 
  1. 112 seconds
  2. 111 seconds
  3. 113 seconds

- Data Processed Per Second:
  1. 0.57142857142857142857 GB/s
  2. 0.57657657657657657657 GB/s
  3. 0.56637168141592920353 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. 6b111dadbcdabed8adf4b1832a06f6fc
  2. 6b111dadbcdabed8adf4b1832a06f6fc
  3. 6b111dadbcdabed8adf4b1832a06f6fc

- Execution Time: 
  1. 69 seconds
  2. 70 seconds
  3. 70 seconds

- Data Processed Per Second:
  1. 0.92753623188405797101 GB/s
  2. 0.91428571428571428571 GB/s
  3. 0.91428571428571428571 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO