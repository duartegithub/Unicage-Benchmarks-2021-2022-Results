# Aggregation Benchmarks: 128 GB

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

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. cccf691e3eed01e036b8e10f919f53fa
  2. cccf691e3eed01e036b8e10f919f53fa
  3. cccf691e3eed01e036b8e10f919f53fa

- Execution Time: 
  1. 959 seconds
  2. 1012 seconds
  3. 964 seconds

- Data Processed Per Second:
  1. 0.13347236704900938477 GB/s
  2. 0.12648221343873517786 GB/s
  3. 0.13278008298755186721 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. cccf691e3eed01e036b8e10f919f53fa
  2. cccf691e3eed01e036b8e10f919f53fa
  3. cccf691e3eed01e036b8e10f919f53fa

- Execution Time: 
  1. 206 seconds
  2. 206 seconds
  3. 204 seconds

- Data Processed Per Second:
  1. 0.62135922330097087378 GB/s
  2. 0.62135922330097087378 GB/s
  3. 0.62745098039215686274 GB/s


### ***Unicage***

- Implementation: [boaAggregation.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregation.sh)

- Output Hash:
  1. cccf691e3eed01e036b8e10f919f53fa
  2. cccf691e3eed01e036b8e10f919f53fa
  3. cccf691e3eed01e036b8e10f919f53fa

- Execution Time: 
  1. 167 seconds
  2. 166 seconds
  3. 167 seconds

- Data Processed Per Second:
  1. 0.76646706586826347305 GB/s
  2. 0.77108433734939759036 GB/s
  3. 0.76646706586826347305 GB/s


---
## Special Considerations:

- The full version of the data generation and loading nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO