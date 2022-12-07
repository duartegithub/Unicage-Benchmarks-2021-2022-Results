# Aggregation Benchmarks: 256 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 280.79 GB (172.71 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 280.79 GB (172.71 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 280.79 GB (172.71 GB of OS_ORDER_ITEM tables) (extra 2)
  4. 280.79 GB (172.71 GB of OS_ORDER_ITEM tables) (extra 3)

- Generation Time:
  1. 1592 seconds
  2. 1591 seconds (extra 1)
  3. 1583 seconds (extra 2)
  4. 1641 seconds (extra 3)

- Loading Time (HDFS):
  1. 1456 seconds (1074 seconds to import as Hive tables)
  2. 1457 seconds (1077 seconds to import as Hive tables) (extra 1)
  3. 1467 seconds (1088 seconds to import as Hive tables) (extra 2)
  4. 1476 seconds (1093 seconds to import as Hive tables) (extra 3)

- Loading Time (Unicage):
  1. 572 seconds
  2. 342 seconds (extra 1)
  3. 343 seconds (extra 2)
  4. 343 seconds (extra 3)


### ***Hive***

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. f87c0114e157b0ab7a5a396f0feacf6a
  2. f87c0114e157b0ab7a5a396f0feacf6a
  3. f87c0114e157b0ab7a5a396f0feacf6a

- Execution Time: 
  1. 2106 seconds
  2. 2156 seconds
  3. 2228 seconds

- Data Processed Per Second: 
  1. 0.12155745489078822412 GB/s
  2. 0.11873840445269016697 GB/s
  3. 0.11490125673249551166 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. f87c0114e157b0ab7a5a396f0feacf6a
  2. f87c0114e157b0ab7a5a396f0feacf6a
  3. f87c0114e157b0ab7a5a396f0feacf6a

- Execution Time: 
  1. 375 seconds
  2. 376 seconds
  3. 372 seconds

- Data Processed Per Second:
  1. 0.68266666666666666666 GB/s
  2. 0.68085106382978723404 GB/s
  3. 0.68817204301075268817 GB/s


### ***Unicage***

- Implementation: [boaAggregation.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregation.sh)

- Output Hash:
  1. f87c0114e157b0ab7a5a396f0feacf6a
  2. f87c0114e157b0ab7a5a396f0feacf6a
  3. f87c0114e157b0ab7a5a396f0feacf6a

- Execution Time: 
  1. 347 seconds
  2. 348 seconds
  3. 348 seconds

- Data Processed Per Second:
  1. 0.73775216138328530259 GB/s
  2. 0.73563218390804597701 GB/s
  3. 0.73563218390804597701 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO