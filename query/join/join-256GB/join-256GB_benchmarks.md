# Join Benchmarks: 256 GB

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

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. 6aa7478917f73c32913205f1e96d79bf
  2. 6aa7478917f73c32913205f1e96d79bf
  3. 6aa7478917f73c32913205f1e96d79bf

- Execution Time: 
  1. 2827 seconds
  2. 3055 seconds
  3. 2802 seconds

- Data Processed Per Second:
  1. 0.09055535903784931022 GB/s
  2. 0.08379705400981996726 GB/s
  3. 0.09136331192005710206 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. 6aa7478917f73c32913205f1e96d79bf
  2. 6aa7478917f73c32913205f1e96d79bf
  3. 6aa7478917f73c32913205f1e96d79bf

- Execution Time: 
  1. 1462 seconds
  2. 1463 seconds
  3. 1479 seconds

- Data Processed Per Second:
  1. 0.17510259917920656634 GB/s
  2. 0.17498291182501708817 GB/s
  3. 0.17308992562542258282 GB/s


### ***Unicage***

- Implementation: [tukubaiJoin.sh](../../../../../workloads/query/interactive/bashQuery/join/tukubaiJoin.sh)

- Output Hash:
  1. c2defc40b1dac5166126330c44019947
  2. c2defc40b1dac5166126330c44019947
  3. c2defc40b1dac5166126330c44019947

- Execution Time: 
  1. 37535 seconds
  2. 36144 seconds
  3. 38493 seconds

- Data Processed Per Second:
  1. 0.00682030105235113893 GB/s
  2. 0.00708277999114652501 GB/s
  3. 0.00665055984204920375 GB/s


---
## Special Considerations:

- Unicage was not in agreement with Spark or Hadoop.


---
## Conclusions:

TODO
