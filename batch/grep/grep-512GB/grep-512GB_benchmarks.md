# Grep Benchmarks: 256 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 501.34 GB (used in the data processing benchmarks below)
  2. 501.13 GB (wordcount)
  3. 501.20 GB (grep-extra)

- Generation Time:
  1. 2961 seconds
  2. 2858 seconds (wordcount)
  3. 2867 seconds (grep-extra)

- Loading Time (HDFS):
  1. 664 seconds
  2. 663 seconds (wordcount)
  3. 664 seconds (grep-extra)

- Loading Time (Unicage):
  1. 736 seconds
  2. 739 seconds (wordcount)
  3. 743 seconds (grep_extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. f7bc892f7dc27ad67c6a6816622d3781
  2. f7bc892f7dc27ad67c6a6816622d3781
  3. f7bc892f7dc27ad67c6a6816622d3781

- Execution Time: 
  1. 1518 seconds
  2. 1505 seconds
  3. 1494 seconds

- Data Processed Per Second:
  1. 0.33728590250329380764 GB/s
  2. 0.34019933554817275747 GB/s
  3. 0.34270414993306559571 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. f7bc892f7dc27ad67c6a6816622d3781
  2. f7bc892f7dc27ad67c6a6816622d3781
  3. f7bc892f7dc27ad67c6a6816622d3781

- Execution Time: 
  1. 685 seconds
  2. 707 seconds
  3. 678 seconds

- Data Processed Per Second:
  1. 0.74744525547445255474 GB/s
  2. 0.72418670438472418670 GB/s
  3. 0.75516224188790560471 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. f7bc892f7dc27ad67c6a6816622d3781
  2. f7bc892f7dc27ad67c6a6816622d3781
  3. f7bc892f7dc27ad67c6a6816622d3781

- Execution Time: 
  1. 539 seconds
  2. 539 seconds
  3. 538 seconds

- Data Processed Per Second:
  1. 0.94990723562152133580 GB/s
  2. 0.94990723562152133580 GB/s
  3. 0.95167286245353159851 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO