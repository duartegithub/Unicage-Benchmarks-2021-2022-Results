# Aggregation Benchmarks: 1024 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 1144.61 GB (698.00 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 1144.61 GB (698.00 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 1144.61 GB (698.00 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 6384 seconds
  2. 6472 seconds (extra 1)
  3. 6436 seconds (extra 2)

- Loading Time (HDFS):
  1. 5813 seconds (4231 seconds to import as Hive tables)
  2. 5860 seconds (4279 seconds to import as Hive tables) (extra 1)
  3. 5865 seconds (4284 seconds to import as Hive tables) (extra 2)

- Loading Time (Unicage):
  1. 1578 seconds
  2. 1575 seconds (extra 1)
  3. 1576 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. a24e1c63b750556c997572d970b54c87
  2. a24e1c63b750556c997572d970b54c87
  3. a24e1c63b750556c997572d970b54c87

- Execution Time: 
  1. 8190 seconds
  2. 7883 seconds
  3. 7902 seconds

- Data Processed Per Second:
  1. 0.12503052503052503052 GB/s
  2. 0.12989978434606114423 GB/s
  3. 0.12958744621614781068 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. a24e1c63b750556c997572d970b54c87
  2. a24e1c63b750556c997572d970b54c87
  3. a24e1c63b750556c997572d970b54c87

- Execution Time: 
  1. 1369 seconds
  2. 1363 seconds
  3. 1372 seconds

- Data Processed Per Second:
  1. 0.74799123447772096420 GB/s
  2. 0.75128393250183418928 GB/s
  3. 0.74635568513119533527 GB/s


### ***Unicage***

- Implementation: [boaAggregationV3.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregationV3.sh)

- Output Hash:
  1. a24e1c63b750556c997572d970b54c87
  2. a24e1c63b750556c997572d970b54c87
  3. a24e1c63b750556c997572d970b54c87

- Execution Time: 
  1. 1972 seconds
  2. 1972 seconds
  3. 1970 seconds

- Data Processed Per Second:
  1. 0.51926977687626774847 GB/s
  2. 0.51926977687626774847 GB/s
  3. 0.51979695431472081218 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO