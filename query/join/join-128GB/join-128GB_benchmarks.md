# Join Benchmarks: 128 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 138.84 GB (85.84 GB of OS_ORDER_ITEM tables) (used in the data processing benchmarks below)
  2. 138.84 GB (85.84 GB of OS_ORDER_ITEM tables) (extra 1)
  3. 138.84 GB (85.84 GB of OS_ORDER_ITEM tables) (extra 2)

- Generation Time:
  1. 807 seconds
  2. 802 seconds (extra 1)
  3. 798 seconds (extra 2)

- Loading Time (HDFS):
  1. 731 seconds (559 seconds to import as Hive tables)
  2. 745 seconds (567 seconds to import as Hive tables) (extra 1)
  3. 734 seconds (560 seconds to import as Hive tables) (extra 2)

- Loading Time (Unicage):
  1. 146 seconds
  2. 166 seconds (extra 1)
  3. 146 seconds (extra 2)


### ***Hive***

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. a9c540d2dba708e6ddd6373214a8547a
  2. a9c540d2dba708e6ddd6373214a8547a
  3. a9c540d2dba708e6ddd6373214a8547a

- Execution Time: 
  1. 1624 seconds
  2. 1697 seconds
  3. 1548 seconds

- Data Processed Per Second:
  1. 0.07881773399014778325 GB/s
  2. 0.07542722451384796700 GB/s
  3. 0.08268733850129198966 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. a9c540d2dba708e6ddd6373214a8547a
  2. a9c540d2dba708e6ddd6373214a8547a
  3. a9c540d2dba708e6ddd6373214a8547a

- Execution Time: 
  1. 594 seconds
  2. 596 seconds
  3. 589 seconds

- Data Processed Per Second:
  1. 0.21548821548821548821 GB/s
  2. 0.21476510067114093959 GB/s
  3. 0.21731748726655348047 GB/s


### ***Unicage***

- Implementation: [tukubaiJoin.sh](../../../../../workloads/query/interactive/bashQuery/join/tukubaiJoin.sh)

- Output Hash:
  1. a9c540d2dba708e6ddd6373214a8547a
  2. a9c540d2dba708e6ddd6373214a8547a
  3. a9c540d2dba708e6ddd6373214a8547a

- Execution Time: 
  1. 13223 seconds
  2. 12680 seconds
  3. 12716 seconds

- Data Processed Per Second:
  1. 0.00968010285109279286 GB/s
  2. 0.01009463722397476340 GB/s
  3. 0.01006605850896508335 GB/s


---
## Special Considerations:

- The full version of the data generation and loading nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO