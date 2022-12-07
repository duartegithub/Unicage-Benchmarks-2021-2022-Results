# Join Benchmarks: 2048 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 2320.33 GB (1406.42 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 2320.33 GB (1406.42 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 2320.33 GB (1406.42 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 12929 seconds
  2. 13135 seconds (extra 1)
  3. 12902 seconds (extra 2)

- Loading Time (HDFS):
  1. 11592 seconds (8440 seconds to import as Hive tables)
  2. 11648 seconds (8498 seconds to import as Hive tables) (extra 1)
  3. 11675 seconds (8521 seconds to import as Hive tables) (extra 2)

- Loading Time (Unicage):
  1. 3155 seconds
  2. 3150 seconds (extra 1)
  3. 3151 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. 9d271937ea08bd98ecb1c3c43594d69a
  2. 9d271937ea08bd98ecb1c3c43594d69a
  3. 9d271937ea08bd98ecb1c3c43594d69a

- Execution Time: 
  1. 18892 seconds
  2. 18990 seconds
  3. 17531 seconds

- Data Processed Per Second:
  1. 0.10840567435951725598 GB/s
  2. 0.10784623486045286993 GB/s
  3. 0.11682163025497689806 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. 9d271937ea08bd98ecb1c3c43594d69a
  2. 9d271937ea08bd98ecb1c3c43594d69a
  3. 9d271937ea08bd98ecb1c3c43594d69a

- Execution Time: 
  1. 14735 seconds
  2. 15441 seconds
  3. 14951 seconds

- Data Processed Per Second:
  1. 0.13898880217170003393 GB/s
  2. 0.13263389676834401916 GB/s
  3. 0.13698080395960136445 GB/s


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