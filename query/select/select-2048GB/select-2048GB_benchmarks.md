# Select Benchmarks: 2048 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. d7d06927579881c912e4d34dad7c86e7
  2. d7d06927579881c912e4d34dad7c86e7
  3. d7d06927579881c912e4d34dad7c86e7

- Execution Time: 
  1. 4770 seconds
  2. 4796 seconds
  3. 4225 seconds

- Data Processed Per Second:
  1. 0.42935010482180293501 GB/s
  2. 0.42944013420004193751 GB/s
  3. 0.48473372781065088757 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. d7d06927579881c912e4d34dad7c86e7
  2. d7d06927579881c912e4d34dad7c86e7
  3. d7d06927579881c912e4d34dad7c86e7

- Execution Time: 
  1. 3194 seconds
  2. 3196 seconds
  3. 3265 seconds

- Data Processed Per Second:
  1. 0.64120225422667501565 GB/s
  2. 0.64080100125156445556 GB/s
  3. 0.62725880551301684532 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. d7d06927579881c912e4d34dad7c86e7
  2. d7d06927579881c912e4d34dad7c86e7
  3. d7d06927579881c912e4d34dad7c86e7

- Execution Time: 
  1. 1504 seconds
  2. 1505 seconds
  3. 1504 seconds

- Data Processed Per Second:
  1. 1.36170212765957446808 GB/s
  2. 1.36079734219269102990 GB/s
  3. 1.36170212765957446808 GB/s


---
## Special Considerations:

Spark's performance fell significantly... RDD recomputing.

---
## Conclusions:

TODO
