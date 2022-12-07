# Join Benchmarks: 512 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 564.68 GB (346.45 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 564.68 GB (346.45 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 564.68 GB (346.45 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 3193 seconds
  2. 3389 seconds (extra 1)
  3. 3197 seconds (extra 2)

- Loading Time (HDFS):
  1. 2854 seconds (2087 seconds to import as Hive tables)
  2. 2905 seconds (2138 seconds to import as Hive tables) (extra 1)
  3. 2908 seconds (2142 seconds to import as Hive tables) (extra 2)

- Loading Time (Unicage):
  1. 749 seconds
  2. 747 seconds (extra 1)
  3. 744 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. dcbb7148d35b744fae4681e21b1755ac
  2. dcbb7148d35b744fae4681e21b1755ac
  3. dcbb7148d35b744fae4681e21b1755ac

- Execution Time: 
  1. 5078 seconds
  2. 5070 seconds
  3. 4936 seconds

- Data Processed Per Second:
  1. 0.10082709728239464356 GB/s
  2. 0.10098619329388560157 GB/s
  3. 0.10372771474878444084 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. dcbb7148d35b744fae4681e21b1755ac
  2. dcbb7148d35b744fae4681e21b1755ac
  3. dcbb7148d35b744fae4681e21b1755ac

- Execution Time: 
  1. 3319 seconds
  2. 3366 seconds
  3. 3367 seconds

- Data Processed Per Second:
  1. 0.15426333232901476348 GB/s
  2. 0.15210932857991681521 GB/s
  3. 0.15206415206415206415 GB/s


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