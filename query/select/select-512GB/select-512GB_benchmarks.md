# Select Benchmarks: 512 GB

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

- Implementation: [e-commerce-select.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-select.sql)

- Output Hash:
  1. 437257ded4d885aa174e39e85dc9bd6a
  2. 437257ded4d885aa174e39e85dc9bd6a
  3. 437257ded4d885aa174e39e85dc9bd6a

- Execution Time: 
  1. 978 seconds
  2. 973 seconds
  3. 984 seconds

- Data Processed Per Second:
  1. 0.52351738241308793456 GB/s
  2. 0.52620760534429599177 GB/s
  3. 0.52032520325203252032 GB/s


### ***Spark***

- Implementation: [Select.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Select.scala)

- Output Hash:
  1. 437257ded4d885aa174e39e85dc9bd6a
  2. 437257ded4d885aa174e39e85dc9bd6a
  3. 437257ded4d885aa174e39e85dc9bd6a

- Execution Time: 
  1. 500 seconds
  2. 501 seconds
  3. 503 seconds

- Data Processed Per Second:
  1. 1.02400000000000000000 GB/s
  2. 1.02195608782435129740 GB/s
  3. 1.01789264413518886679 GB/s


### ***Unicage***

- Implementation: [boaSelect.sh](../../../../../workloads/query/interactive/bashQuery/select/boaSelect/boaSelect.sh)

- Output Hash:
  1. 437257ded4d885aa174e39e85dc9bd6a
  2. 437257ded4d885aa174e39e85dc9bd6a
  3. 437257ded4d885aa174e39e85dc9bd6a

- Execution Time: 
  1. 371 seconds
  2. 370 seconds
  3. 370 seconds

- Data Processed Per Second:
  1. 1.38005390835579514824 GB/s
  2. 1.38378378378378378378 GB/s
  3. 1.38378378378378378378 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO
