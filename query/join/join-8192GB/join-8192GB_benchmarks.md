# Join Benchmarks: 4096 GB

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

- Implementation: [e-commerce-join.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-join.sql)

- Output Hash:
  1. af2171f551d923505339be12980c29f0
  2. af2171f551d923505339be12980c29f0
  3. af2171f551d923505339be12980c29f0

- Execution Time: 
  1. 69300 seconds
  2. 74134 seconds
  3. 70248 seconds

- Data Processed Per Second:
  1. 0.11821067821067821067 GB/s
  2. 0.11050260339385437181 GB/s
  3. 0.11661541965607561781 GB/s


### ***Spark***

- Implementation: [Join.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Join.scala)

- Output Hash:
  1. af2171f551d923505339be12980c29f0
  2. af2171f551d923505339be12980c29f0
  3. af2171f551d923505339be12980c29f0

- Execution Time: 
  1. 61300 seconds
  2. 59982 seconds
  3. 59109 seconds

- Data Processed Per Second:
  1. 0.13363784665579119086 GB/s
  2. 0.13657430562502083958 GB/s
  3. 0.13859141585883706372 GB/s


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

- Spark's nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.

- The structured data-set used in the query processing experiments is generated and loaded in such a way that the increase in the input data-set volume results not in an increase of the number of generated files, but in an increase of size of each generated file, which in turn results in an increase of file blocks per file, when the data-set is loaded into HDFS. If the maximum number of file blocks per file is crossed, an exception is thrown. Given that, by defaul, each block in HDFS has 128 MB of size, and the maximum number of blocks per file is of 10000, a file with more than 1.28 TB is expected to result in such an exception, when loaded into HDFS. This problem surfaced when the 8192 GB query data-set was loaded into HDFS, and the exception was logged in the [nohup.out-maximum-number-of-hdfs-blocks](nohup.out-maximum-number-of-hdfs-blocks) log file. This problem was mitigated by increasing the value of the `dfs.namenode.fs-limits.max-blocks-per-file` property in the [hdfs-site.xml](../../../../../cluster/configs/hadoop/hdfs-site.xml) configuration file.


---
## Conclusions:

TODO