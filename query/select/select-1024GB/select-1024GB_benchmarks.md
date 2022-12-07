# Select Benchmarks: 1024 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. d7700fb6df615d888854e64a2d92741c
  2. d7700fb6df615d888854e64a2d92741c
  3. d7700fb6df615d888854e64a2d92741c

- Execution Time: 
  1. 2334 seconds
  2. 1975 seconds
  3. 1981 seconds

- Data Processed Per Second:
  1. 0.43873179091688089117 GB/s
  2. 0.51848101265822784810 GB/s
  3. 0.51691065118626956082 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. d7700fb6df615d888854e64a2d92741c
  2. d7700fb6df615d888854e64a2d92741c
  3. d7700fb6df615d888854e64a2d92741c

- Execution Time: 
  1. 945 seconds
  2. 946 seconds
  3. 947 seconds

- Data Processed Per Second:
  1. 1.08359788359788359788 GB/s
  2. 1.08245243128964059196 GB/s
  3. 1.08130939809926082365 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. d7700fb6df615d888854e64a2d92741c
  2. d7700fb6df615d888854e64a2d92741c
  3. d7700fb6df615d888854e64a2d92741c

- Execution Time: 
  1. 748 seconds
  2. 746 seconds
  3. 747 seconds

- Data Processed Per Second:
  1. 1.36898395721925133689 GB/s
  2. 1.37265415549597855227 GB/s
  3. 1.37081659973226238286 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO
