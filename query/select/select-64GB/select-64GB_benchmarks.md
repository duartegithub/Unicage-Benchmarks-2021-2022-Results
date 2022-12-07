# Select Benchmarks: 64 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. e88c9d79f2887d47094a6b6ea73cbab6
  2. e88c9d79f2887d47094a6b6ea73cbab6
  3. e88c9d79f2887d47094a6b6ea73cbab6

- Execution Time: 
  1. 153 seconds
  2. 152 seconds
  3. 153 seconds

- Data Processed Per Second: 
  1. 0.41830065359477124183 GB/s
  2. 0.42105263157894736842 GB/s
  3. 0.41830065359477124183 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. e88c9d79f2887d47094a6b6ea73cbab6
  2. e88c9d79f2887d47094a6b6ea73cbab6
  3. e88c9d79f2887d47094a6b6ea73cbab6

- Execution Time: 
  1. 92 seconds
  2. 91 seconds
  3. 91 seconds

- Data Processed Per Second:
  1. 0.69565217391304347826 GB/s
  2. 0.70329670329670329670 GB/s
  3. 0.70329670329670329670 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. e88c9d79f2887d47094a6b6ea73cbab6
  2. e88c9d79f2887d47094a6b6ea73cbab6
  3. e88c9d79f2887d47094a6b6ea73cbab6

- Execution Time: 
  1. 46 seconds
  2. 45 seconds
  3. 45 seconds

- Data Processed Per Second:
  1. 1.39130434782608695652 GB/s
  2. 1.42222222222222222222 GB/s
  3. 1.42222222222222222222 GB/s


---
## Special Considerations:

- The full version of the data generation and loading nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO