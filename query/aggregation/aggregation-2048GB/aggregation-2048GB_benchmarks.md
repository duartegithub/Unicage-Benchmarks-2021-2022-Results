# Aggregation Benchmarks: 2048 GB

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

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. 3ba324789c97475c12c627dbfa5069ea
  2. 3ba324789c97475c12c627dbfa5069ea
  3. 3ba324789c97475c12c627dbfa5069ea

- Execution Time: 
  1. 15819 seconds
  2. 16613 seconds
  3. 15447 seconds

- Data Processed Per Second:
  1. 0.12946456792464757570 GB/s
  2. 0.12327695178474688496 GB/s
  3. 0.13258237845536350100 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. 3ba324789c97475c12c627dbfa5069ea
  2. 3ba324789c97475c12c627dbfa5069ea
  3. 3ba324789c97475c12c627dbfa5069ea

- Execution Time: 
  1. 3858 seconds
  2. 3896 seconds
  3. 3938 seconds

- Data Processed Per Second:
  1. 0.53084499740798341109 GB/s
  2. 0.52566735112936344969 GB/s
  3. 0.52006094464195022854 GB/s


### ***Unicage***

- Implementation: [boaAggregationV3.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregationV3.sh)

- Output Hash:
  1. 3ba324789c97475c12c627dbfa5069ea
  2. 3ba324789c97475c12c627dbfa5069ea
  3. 3ba324789c97475c12c627dbfa5069ea

- Execution Time: 
  1. 4055 seconds
  2. 4048 seconds
  3. 4060 seconds

- Data Processed Per Second:
  1. 0.50505548705302096177 GB/s
  2. 0.50592885375494071146 GB/s
  3. 0.50443349753694581280 GB/s


---
## Special Considerations:

Spark's performance fell significantly... RDD recomputing.


---
## Conclusions:

TODO