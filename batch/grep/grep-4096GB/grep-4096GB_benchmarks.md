# Grep Benchmarks: 4096 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 4009.08 GB (used in the data processing benchmarks below)
  2. 4008.87 GB (wordcount)
  3. 4008.95 GB (grep-extra)

- Generation Time:
  1. 23620 seconds
  2. 22811 seconds (wordcount)
  3. 22893 seconds (grep-extra)

- Loading Time (HDFS):
  1. 5370 seconds
  2. 5352 seconds (wordcount)
  3. 5367 seconds (grep-extra)

- Loading Time (Unicage):
  1. 6272 seconds
  2. 6202 seconds (wordcount)
  3. 6195 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 174f09f0ec84a9b72f7d555ec0ede946
  2. 174f09f0ec84a9b72f7d555ec0ede946
  3. 174f09f0ec84a9b72f7d555ec0ede946

- Execution Time: 
  1. 11897 seconds
  2. 11830 seconds
  3. 11926 seconds

- Data Processed Per Second:
  1. 0.34428847608640833823 GB/s
  2. 0.34623837700760777683 GB/s
  3. 0.34345128291128626530 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. 174f09f0ec84a9b72f7d555ec0ede946
  2. 174f09f0ec84a9b72f7d555ec0ede946
  3. 174f09f0ec84a9b72f7d555ec0ede946

- Execution Time: 
  1. 5341 seconds
  2. 5502 seconds
  3. 5293 seconds

- Data Processed Per Second:
  1. 0.76689758472196217936 GB/s
  2. 0.74445656125045438022 GB/s
  3. 0.77385225769884753447 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. 174f09f0ec84a9b72f7d555ec0ede946
  2. 174f09f0ec84a9b72f7d555ec0ede946
  3. 174f09f0ec84a9b72f7d555ec0ede946

- Execution Time: 
  1. 4289 seconds
  2. 4289 seconds
  3. 4293 seconds

- Data Processed Per Second:
  1. 0.95500116577290743763 GB/s
  2. 0.95500116577290743763 GB/s
  3. 0.95411134404845096668 GB/s


---
## Special Considerations:

- Spark's nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO