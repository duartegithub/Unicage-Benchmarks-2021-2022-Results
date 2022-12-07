# Grep Benchmarks: 2048 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 2004.82 GB (used in the data processing benchmarks below)
  2. 2004.76 GB (wordcount)
  3. 2004.72 GB (grep-extra)

- Generation Time:
  1. 11855 seconds
  2. 11429 seconds (wordcount)
  3. 11436 seconds (grep-extra)

- Loading Time (HDFS):
  1. 2671 seconds
  2. 2667 seconds (wordcount)
  3. 2659 seconds (grep-extra)

- Loading Time (Unicage):
  1. 3248 seconds
  2. 3081 seconds (wordcount)
  3. 3079 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. f634a37c2f23da1afb5a46ad9c53f4e4
  2. f634a37c2f23da1afb5a46ad9c53f4e4
  3. f634a37c2f23da1afb5a46ad9c53f4e4

- Execution Time: 
  1. 5906 seconds
  2. 5889 seconds
  3. 5891 seconds

- Data Processed Per Second: 
  1. 0.34676600067727734507 GB/s
  2. 0.34776702326371200543 GB/s
  3. 0.34764895603462909523 GB/s


### ***Spark***

- Implementation: [Grep.scala](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. f634a37c2f23da1afb5a46ad9c53f4e4
  2. f634a37c2f23da1afb5a46ad9c53f4e4
  3. f634a37c2f23da1afb5a46ad9c53f4e4

- Execution Time: 
  1. 2731 seconds
  2. 2643 seconds
  3. 2640 seconds

- Data Processed Per Second:
  1. 0.74990845844013181984 GB/s
  2. 0.77487703367385546727 GB/s
  3. 0.77575757575757575757 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. f634a37c2f23da1afb5a46ad9c53f4e4
  2. f634a37c2f23da1afb5a46ad9c53f4e4
  3. f634a37c2f23da1afb5a46ad9c53f4e4

- Execution Time: 
  1. 2147 seconds
  2. 2146 seconds
  3. 2146 seconds

- Data Processed Per Second:
  1. 0.95388914764788076385 GB/s
  2. 0.95433364398881640260 GB/s
  3. 0.95433364398881640260 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO