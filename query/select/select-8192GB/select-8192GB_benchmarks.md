# Select Benchmarks: 8192 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 9416.87 GB (5671.80 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 9416.87 GB (5671.80 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 9416.87 GB (5671.80 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 51278 seconds
  2. 51904 seconds (extra 1)
  3. 51355 seconds (extra 2)

- Loading Time (HDFS):
  1. 46906 seconds (33903 seconds to import as Hive tables)
  2. 46532 seconds (33541 seconds to import as Hive tables) (extra 1)
  3. 55205 seconds (42387 seconds to import as HIve tables) (extra 2)

- Loading Time (Unicage):
  1. 12795 seconds
  2. 13168 seconds (extra 1)
  3. 13124 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. d4491a79f3d6786d0fec601d8a5d9852
  2. d4491a79f3d6786d0fec601d8a5d9852
  3. d4491a79f3d6786d0fec601d8a5d9852

- Execution Time: 
  1. 25454 seconds
  2. 25149 seconds
  3. 25531 seconds

- Data Processed Per Second:
  1. 0.32183546790288363322 GB/s
  2. 0.32573859795618116028 GB/s
  3. 0.32086483098977713368 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. d4491a79f3d6786d0fec601d8a5d9852
  2. d4491a79f3d6786d0fec601d8a5d9852
  3. d4491a79f3d6786d0fec601d8a5d9852

- Execution Time: 
  1. 13397 seconds
  2. 13147 seconds
  3. 12854 seconds

- Data Processed Per Second:
  1. 0.61148018213032768530 GB/s
  2. 0.62310793336882939073 GB/s
  3. 0.63731134277267776567 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. d4491a79f3d6786d0fec601d8a5d9852
  2. d4491a79f3d6786d0fec601d8a5d9852
  3. d4491a79f3d6786d0fec601d8a5d9852

- Execution Time: 
  1. 6066 seconds
  2. 6065 seconds
  3. 6065 seconds

- Data Processed Per Second:
  1. 1.35047807451368282228 GB/s
  2. 1.35070074196207749381 GB/s
  3. 1.35070074196207749381 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO