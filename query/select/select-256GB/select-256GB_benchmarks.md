# Select Benchmarks: 256 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. 9dd9689eb3c143508788a92e23b10399
  2. 9dd9689eb3c143508788a92e23b10399
  3. 9dd9689eb3c143508788a92e23b10399

- Execution Time: 
  1. 498 seconds
  2. 499 seconds
  3. 497 seconds

- Data Processed Per Second:
  1. 0.51405622489959839357 GB/s
  2. 0.51302605210420841683 GB/s
  3. 0.51509054325955734406 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. 9dd9689eb3c143508788a92e23b10399
  2. 9dd9689eb3c143508788a92e23b10399
  3. 9dd9689eb3c143508788a92e23b10399

- Execution Time: 
  1. 270 seconds
  2. 268 seconds
  3. 271 seconds

- Data Processed Per Second:
  1. 0.94814814814814814814 GB/s
  2. 0.95522388059701492537 GB/s
  3. 0.94464944649446494464 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. 9dd9689eb3c143508788a92e23b10399
  2. 9dd9689eb3c143508788a92e23b10399
  3. 9dd9689eb3c143508788a92e23b10399

- Execution Time: 
  1. 185 seconds
  2. 185 seconds
  3. 185 seconds

- Data Processed Per Second:
  1. 1.38378378378378378378 GB/s
  2. 1.38378378378378378378 GB/s
  3. 1.38378378378378378378 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO