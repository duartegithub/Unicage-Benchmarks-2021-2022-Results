# Aggregation Benchmarks: 4096 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 4671.93 GB (2823.43 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 4671.93 GB (2823.43 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 4671.93 GB (2823.43 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 25390 seconds
  2. 25944 seconds (extra 1)
  3. 25670 seconds (extra 2)

- Loading Time (HDFS):
  1. 23171 seconds (16882 seconds to import as Hive tables)
  2. 27097 seconds (20801 seconds to import as Hive tables) (extra 1)
  3. 23406 seconds (17118 seconds to import as Hive tables) (extra 2)

- Loading Time (Unicage):
  1. 6292 seconds
  2. 6499 seconds (extra 1)
  3. 6289 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. 8b8e957d6a8700d311c56e0baee4162
  2. 8b8e957d6a8700d311c56e0baee4162
  3. 8b8e957d6a8700d311c56e0baee4162

- Execution Time: 
  1. 30227 seconds
  2. 30554 seconds
  3. 29241 seconds

- Data Processed Per Second:
  1. 0.13550798954577033777 GB/s
  2. 0.13405773384826863913 GB/s
  3. 0.14007728873841523887 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. 8b8e957d6a8700d311c56e0baee4162
  2. 8b8e957d6a8700d311c56e0baee4162
  3. 8b8e957d6a8700d311c56e0baee4162

- Execution Time: 
  1. 7890 seconds
  2. 7771 seconds
  3. 7779 seconds

- Data Processed Per Second:
  1. 0.51913814955640050697 GB/s
  2. 0.52708789087633509200 GB/s
  3. 0.52654582851266229592 GB/s


### ***Unicage***

- Implementation: [boaAggregationV3.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregationV3.sh)

- Output Hash:
  1. 8b8e957d6a8700d311c56e0baee4162
  2. 8b8e957d6a8700d311c56e0baee4162
  3. 8b8e957d6a8700d311c56e0baee4162

- Execution Time: 
  1. 8272 seconds
  2. 8442 seconds
  3. 8339 seconds

- Data Processed Per Second:
  1. 0.49516441005802707930 GB/s
  2. 0.48519308220800758114 GB/s
  3. 0.49118599352440340568 GB/s


---
## Special Considerations:

TODO

---
## Conclusions:

TODO