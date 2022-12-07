# Grep Benchmarks: 256 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 250.63 GB (used in the data processing benchmarks below)
  2. 250.57 GB (wordcount)
  3. 250.79 GB (grep-extra)

- Generation Time:
  1. 1483 seconds
  2. 1430 seconds (wordcount)
  3. 1436 seconds (grep-extra)

- Loading Time (HDFS):
  1. 316 seconds
  2. 321 seconds (wordcount)
  3. 316 seconds (grep-extra)

- Loading Time (Unicage):
  1. 343 seconds
  2. 336 seconds (wordcount)
  3. 347 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 53752d41c73f71193d62ca734a381c3b
  2. 53752d41c73f71193d62ca734a381c3b
  3. 53752d41c73f71193d62ca734a381c3b

- Execution Time: 
  1. 776 seconds
  2. 773 seconds
  3. 773 seconds

- Data Processed Per Second: 
  1. 0.32989690721649484536 GB/s
  2. 0.33117723156532988357 GB/s
  3. 0.33117723156532988357 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. 53752d41c73f71193d62ca734a381c3b
  2. 53752d41c73f71193d62ca734a381c3b
  3. 53752d41c73f71193d62ca734a381c3b

- Execution Time: 
  1. 383 seconds
  2. 362 seconds
  3. 361 seconds

- Data Processed Per Second:
  1. 0.66840731070496083550 GB/s
  2. 0.70718232044198895027 GB/s
  3. 0.70914127423822714681 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. 53752d41c73f71193d62ca734a381c3b
  2. 53752d41c73f71193d62ca734a381c3b
  3. 53752d41c73f71193d62ca734a381c3b

- Execution Time: 
  1. 271 seconds
  2. 271 seconds
  3. 270 seconds

- Data Processed Per Second: 
  1. 0.94464944649446494464 GB/s
  2. 0.94464944649446494464 GB/s
  3. 0.94814814814814814814 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO