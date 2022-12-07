# Join Benchmarks: 1024 GB

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

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. c747eeec8188097dd73c5cda0c648a71
  2. c747eeec8188097dd73c5cda0c648a71
  3. c747eeec8188097dd73c5cda0c648a71

- Execution Time: 
  1. 9779 seconds
  2. 10549 seconds
  3. 9032 seconds

- Data Processed Per Second:
  1. 0.10474631751227495908 GB/s
  2. 0.09707081239927955256 GB/s
  3. 0.11337466784765279007 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. c747eeec8188097dd73c5cda0c648a71
  2. c747eeec8188097dd73c5cda0c648a71
  3. c747eeec8188097dd73c5cda0c648a71

- Execution Time: 
  1. 7346 seconds
  2. 7179 seconds
  3. 7311 seconds

- Data Processed Per Second:
  1. 0.13939558943642798802 GB/s
  2. 0.14263825045270929098 GB/s
  3. 0.14006291888934482286 GB/s


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