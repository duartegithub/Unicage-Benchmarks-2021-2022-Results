# Wordcount Benchmarks: 128 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 125.23 GB (grep)
  2. 125.24 GB (used in the data processing benchmarks below)
  3. 125.28 GB (grep-extra)

- Generation Time:
  1. 768 seconds (grep)
  2. 736 seconds 
  3. 737 seconds (grep-extra)

- Loading Time (HDFS):
  1. 137 seconds (grep)
  2. 144 seconds 
  3. 134 seconds (grep-extra)

- Loading Time (Unicage):
  1. 150 seconds (grep)
  2. 150 seconds 
  3. 162 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/wordcount/javaWordcount/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. 917d1245cc2c87b001e717eda5508812
  2. 917d1245cc2c87b001e717eda5508812
  3. 917d1245cc2c87b001e717eda5508812

- Execution Time: 
  1. 2165 seconds
  2. 2162 seconds
  3. 2143 seconds

- Data Processed Per Second:
  1. 0.05912240184757505773 GB/s
  2. 0.05920444033302497687 GB/s
  3. 0.05972935137657489500 GB/s


### ***Spark***

- Implementation: [Wordcount.scala](../../../../../workloads/batch/wordcount/scalaWordcount/src/main/scala/WordCount.scala%20(buffer%20overflow))

- Output Hash:
  1. 917d1245cc2c87b001e717eda5508812
  2. 917d1245cc2c87b001e717eda5508812
  3. 917d1245cc2c87b001e717eda5508812

- Execution Time: 
  1. 375 seconds
  2. 365 seconds
  3. 372 seconds

- Data Processed Per Second: 
  1. 0.34133333333333333333 GB/s
  2. 0.35068493150684931506 GB/s
  3. 0.34408602150537634408 GB/s


### ***Unicage***

- Implementation: [boaWordcount.sh](../../../../../workloads/batch/wordcount/bashWordcount/boaWordcount/boaWordcount.sh)

- Output Hash:
  1. 917d1245cc2c87b001e717eda5508812
  2. 917d1245cc2c87b001e717eda5508812
  3. 917d1245cc2c87b001e717eda5508812

- Execution Time: 
  1. 627 seconds
  2. 629 seconds
  3. 652 seconds

- Data Processed Per Second:
  1. 0.20414673046251993620 GB/s
  2. 0.20349761526232114467 GB/s
  3. 0.19631901840490797546 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO