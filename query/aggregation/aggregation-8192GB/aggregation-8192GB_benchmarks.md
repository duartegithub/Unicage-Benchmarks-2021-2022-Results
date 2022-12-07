# Aggregation Benchmarks: 8192 GB

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

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. Unable to finish
  2. Unable to finish
  3. Unable to finish

- Execution Time: 
  1. Unable to finish
  2. Unable to finish
  3. Unable to finish

- Data Processed Per Second:
  1. Unable to finish
  2. Unable to finish
  3. Unable to finish


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. a6eaf452008b09058220d48b3f30f0ed
  2. a6eaf452008b09058220d48b3f30f0ed
  3. a6eaf452008b09058220d48b3f30f0ed

- Execution Time: 
  1. 15714 seconds
  2. 15741 seconds
  3. 15645 seconds

- Data Processed Per Second:
  1. 0.52131856942853506427 GB/s
  2. 0.52042436948097325455 GB/s
  3. 0.52361776925535314797 GB/s


### ***Unicage***

- Implementation: [boaAggregationV3.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregationV3.sh)

- Output Hash:
  1. a6eaf452008b09058220d48b3f30f0ed
  2. a6eaf452008b09058220d48b3f30f0ed
  3. a6eaf452008b09058220d48b3f30f0ed

- Execution Time: 
  1. 17075 seconds
  2. 17095 seconds
  3. 17036 seconds

- Data Processed Per Second:
  1. 0.47976573938506588579 GB/s
  2. 0.47920444574436969874 GB/s
  3. 0.48086405259450575252 GB/s


---
## Special Considerations:

- The structured data-set used in the query processing experiments is generated and loaded in such a way that the increase in the input data-set volume results not in an increase of the number of generated files, but in an increase of size of each generated file, which in turn results in an increase of file blocks per file, when the data-set is loaded into HDFS. If the maximum number of file blocks per file is crossed, an exception is thrown. Given that, by defaul, each block in HDFS has 128 MB of size, and the maximum number of blocks per file is of 10000, a file with more than 1.28 TB is expected to result in such an exception, when loaded into HDFS. This problem surfaced when the 8192 GB query data-set was loaded into HDFS, and the exception was logged in the [nohup.out-maximum-number-of-hdfs-blocks](nohup.out-maximum-number-of-hdfs-blocks) log file. This problem was mitigated by increasing the value of the `dfs.namenode.fs-limits.max-blocks-per-file` property in the [hdfs-site.xml](../../../../../cluster/configs/hadoop/hdfs-site.xml) configuration file.

- Hive was not able to finish this workload, as it was stuck in the first stage of MapReduce. THis is logged in the [nohup.out-maximum-number-of-hdfs-blocks](./nohup.out-maximum-number-of-hdfs-blocks) log file.


---
## Conclusions:

TODO