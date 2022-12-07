# Aggregation Benchmarks: 64 GB

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

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. 61c169965f44408d7a12b12cc3bb0a96
  2. 61c169965f44408d7a12b12cc3bb0a96
  3. 61c169965f44408d7a12b12cc3bb0a96

- Execution Time: 
  1. 494 seconds
  2. 493 seconds
  3. 512 seconds

- Data Processed Per Second:
  1. 0.12955465587044534412 GB/s
  2. 0.12981744421906693711 GB/s
  3. 0.12500000000000000000 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. 61c169965f44408d7a12b12cc3bb0a96
  2. 61c169965f44408d7a12b12cc3bb0a96
  3. 61c169965f44408d7a12b12cc3bb0a96

- Execution Time: 
  1. 123 seconds
  2. 122 seconds
  3. 120 seconds

- Data Processed Per Second:
  1. 0.52032520325203252032 GB/s
  2. 0.52459016393442622950 GB/s
  3. 0.53333333333333333333 GB/s


### ***Unicage***

- Implementation: [boaAggregation.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregation.sh)

- Output Hash:
  1. 61c169965f44408d7a12b12cc3bb0a96
  2. 61c169965f44408d7a12b12cc3bb0a96
  3. 61c169965f44408d7a12b12cc3bb0a96

- Execution Time: 
  1. 81 seconds
  2. 79 seconds
  3. 81 seconds

- Data Processed Per Second:
  1. 0.79012345679012345679 GB/s
  2. 0.81012658227848101265 GB/s
  3. 0.79012345679012345679 GB/s


---
## Special Considerations:

- The full version of the data generation and loading nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO
