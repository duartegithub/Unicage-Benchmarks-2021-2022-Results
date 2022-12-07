# Join Benchmarks: 64 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 68.16 GB (42.50 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 68.16 GB (42.50 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 68.16 GB (42.50 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 419 seconds
  2. 393 seconds (extra 1)
  3. 399 seconds (extra 2)

- Loading Time (HDFS):
  1. 396 seconds (315 seconds to import as Hive tables)
  2. 401 seconds (319 seconds to import as Hive tables) (extra 1)
  3. 393 seconds (312 seconds to import as Hive tables) (extra 2)

- Loading Time (Unicage):
  1. 65 seconds
  2. 64 seconds (extra 1)
  3. 68 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. 579d93cd8b1d84969e0e8f0d39d820a3
  2. 579d93cd8b1d84969e0e8f0d39d820a3
  3. 579d93cd8b1d84969e0e8f0d39d820a3

- Execution Time: 
  1. 827 seconds
  2. 762 seconds
  3. 791 seconds

- Data Processed Per Second:
  1. 0.07738814993954050785 GB/s
  2. 0.08398950131233595800 GB/s
  3. 0.08091024020227560050 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. 579d93cd8b1d84969e0e8f0d39d820a3
  2. 579d93cd8b1d84969e0e8f0d39d820a3
  3. 579d93cd8b1d84969e0e8f0d39d820a3

- Execution Time: 
  1. 277 seconds
  2. 286 seconds
  3. 286 seconds

- Data Processed Per Second:
  1. 0.23104693140794223826 GB/s
  2. 0.22377622377622377622 GB/s
  3. 0.22377622377622377622 GB/s


### ***Unicage***

- Implementation: [tukubaiJoin.sh](../../../../../workloads/query/interactive/bashQuery/join/tukubaiJoin.sh)

- Output Hash:
  1. 579d93cd8b1d84969e0e8f0d39d820a3
  2. 579d93cd8b1d84969e0e8f0d39d820a3
  3. 579d93cd8b1d84969e0e8f0d39d820a3

- Execution Time: 
  1. 5826 seconds
  2. 5919 seconds
  3. 6030 seconds

- Data Processed Per Second:
  1. 0.01098523858565053209 GB/s
  2. 0.01081263726980908937 GB/s
  3. 0.01061359867330016583 GB/s


---
## Special Considerations:

- The full version of the data generation and loading nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO