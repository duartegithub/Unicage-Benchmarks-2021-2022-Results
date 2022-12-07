# Select Benchmarks: 4096 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. 2e1eb0e4a579bfe0e3cf392b035228ac
  2. 2e1eb0e4a579bfe0e3cf392b035228ac
  3. 2e1eb0e4a579bfe0e3cf392b035228ac

- Execution Time: 
  1. 10443 seconds
  2. 10470 seconds
  3. 10565 seconds

- Data Processed Per Second:
  1. 0.39222445657378148041 GB/s
  2. 0.39121298949379178605 GB/s
  3. 0.38769522006625650733 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. 2e1eb0e4a579bfe0e3cf392b035228ac
  2. 2e1eb0e4a579bfe0e3cf392b035228ac
  3. 2e1eb0e4a579bfe0e3cf392b035228ac

- Execution Time: 
  1. 6245 seconds
  2. 6170 seconds
  3. 6164 seconds

- Data Processed Per Second:
  1. 0.65588470776621297037 GB/s
  2. 0.66385737439222042139 GB/s
  3. 0.66450356911096690460 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. 2e1eb0e4a579bfe0e3cf392b035228ac
  2. 2e1eb0e4a579bfe0e3cf392b035228ac
  3. 2e1eb0e4a579bfe0e3cf392b035228ac

- Execution Time: 
  1. 3021 seconds
  2. 3019 seconds
  3. 3019 seconds

- Data Processed Per Second:
  1. 1.35584243627937768950 GB/s
  2. 1.35674064259688638622 GB/s
  3. 1.35674064259688638622 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO
