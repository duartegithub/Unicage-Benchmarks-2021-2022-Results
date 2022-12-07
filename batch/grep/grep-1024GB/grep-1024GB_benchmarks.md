# Grep Benchmarks: 1024 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 1002.10 GB (used in the data processing benchmarks below)
  2. 1002.19 GB (wordcount)
  3. 1002.26 GB (grep-extra)

- Generation Time:
  1. 5884 seconds
  2. 5711 seconds (wordcount)
  3. 5723 seconds (grep-extra)

- Loading Time (HDFS):
  1. 1340 seconds
  2. 1343 seconds (wordcount)
  3. 1341 seconds (grep-extra)

- Loading Time (Unicage):
  1. 1521 seconds
  2. 1525 seconds (wordcount)
  3. 1519 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 80971237267e322097fa12d00cd5149c
  2. 80971237267e322097fa12d00cd5149c
  3. 80971237267e322097fa12d00cd5149c

- Execution Time: 
  1. 2968 seconds
  2. 2971 seconds
  3. 2969 seconds

- Data Processed Per Second:
  1. 0.34501347708894878706 GB/s
  2. 0.34466509592729720632 GB/s
  3. 0.34489727180868979454 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. 80971237267e322097fa12d00cd5149c
  2. 80971237267e322097fa12d00cd5149c
  3. 80971237267e322097fa12d00cd5149c

- Execution Time: 
  1. 1370 seconds
  2. 1363 seconds
  3. 1343 seconds

- Data Processed Per Second:
  1. 0.74744525547445255474 GB/s
  2. 0.75128393250183418928 GB/s
  3. 0.76247207743857036485 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. 80971237267e322097fa12d00cd5149c
  2. 80971237267e322097fa12d00cd5149c
  3. 80971237267e322097fa12d00cd5149c

- Execution Time: 
  1. 1075 seconds
  2. 1074 seconds
  3. 1075 seconds

- Data Processed Per Second:
  1. 0.95255813953488372093 GB/s
  2. 0.95344506517690875232 GB/s
  3. 0.95255813953488372093 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO