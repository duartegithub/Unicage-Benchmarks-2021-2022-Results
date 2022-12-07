# Select Benchmarks: 128 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. 6ef39af889379ab9b53e038d1c70b750
  2. 6ef39af889379ab9b53e038d1c70b750
  3. 6ef39af889379ab9b53e038d1c70b750

- Execution Time: 
  1. 267 seconds
  2. 265 seconds
  3. 267 seconds

- Data Processed Per Second:
  1. 0.47940074906367041198 GB/s
  2. 0.48301886792452830188 GB/s
  3. 0.47940074906367041198 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. 6ef39af889379ab9b53e038d1c70b750
  2. 6ef39af889379ab9b53e038d1c70b750
  3. 6ef39af889379ab9b53e038d1c70b750

- Execution Time: 
  1. 147 seconds
  2. 148 seconds
  3. 148 seconds

- Data Processed Per Second:
  1. 0.87074829931972789115 GB/s
  2. 0.86486486486486486486 GB/s
  3. 0.86486486486486486486 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. 6ef39af889379ab9b53e038d1c70b750
  2. 6ef39af889379ab9b53e038d1c70b750
  3. 6ef39af889379ab9b53e038d1c70b750

- Execution Time: 
  1. 92 seconds
  2. 92 seconds
  3. 92 seconds

- Data Processed Per Second:
  1. 1.39130434782608695652 GB/s
  2. 1.39130434782608695652 GB/s
  3. 1.39130434782608695652 GB/s


---
## Special Considerations:

- The full version of the data generation and loading nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.


---
## Conclusions:

TODO