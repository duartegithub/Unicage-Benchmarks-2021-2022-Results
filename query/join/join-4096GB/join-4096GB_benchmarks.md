# Join Benchmarks: 4096 GB

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

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. 4e03003d109eb8ecf753a4ad7da82954
  2. 4e03003d109eb8ecf753a4ad7da82954
  3. 4e03003d109eb8ecf753a4ad7da82954

- Execution Time: 
  1. 38397 seconds
  2. 36747 seconds
  3. 37377 seconds

- Data Processed Per Second:
  1. 0.10667500065109253327 GB/s
  2. 0.11146488148692410264 GB/s
  3. 0.10958610910452952350 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. 4e03003d109eb8ecf753a4ad7da82954
  2. 4e03003d109eb8ecf753a4ad7da82954
  3. 4e03003d109eb8ecf753a4ad7da82954

- Execution Time: 
  1. 29853 seconds
  2. 30558 seconds
  3. 30316 seconds

- Data Processed Per Second:
  1. 0.13720564097410645496 GB/s
  2. 0.13404018587603900778 GB/s
  3. 0.13511017284602190262 GB/s


### ***Unicage***

- Output Hash:
  1. TODO
  2. TODO
  3. TODO

- Execution Time: 
  1. TODO
  2. TODO
  3. TODO

- Data Processed Per Second:
  1. TODO
  2. TODO
  3. TODO


---
## Special Considerations:

TODO


---
## Conclusions:

TODO