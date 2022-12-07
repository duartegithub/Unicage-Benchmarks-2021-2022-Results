# Sort Benchmarks: 128 GB

---
## Benchmark Results:

- Generation Time:
  1. 980 seconds
  2. TODO
  3. TODO

- Loading Time (HDFS):
  1. 136 seconds
  2. TODO
  3. TODO

- Loading Time (Unicage):
  1. 175 seconds
  2. TODO
  3. TODO


### ***Hadoop***

- Implementation: [Sort.java](../../../../../workloads/batch/sort/javaSort/Sort/src/main/java/Sort.java)

- Output Hash:
  1. b86a7517426286535761a14ca8504cb9
  2. b86a7517426286535761a14ca8504cb9
  3. b86a7517426286535761a14ca8504cb9

- Execution Time: 
  1. 27788 seconds
  2. 27850 seconds
  3. 28043 seconds

- Data Processed Per Second:
  1. 0.00460630487980423204 GB/s
  2. 0.00459605026929982046 GB/s
  3. 0.00456441892807474235 GB/s


### ***Spark***

- Implementation: [Sort.scala](../../../../../workloads/batch/sort/scalaSort/src/main/scala/Sort.scala)

- Output Hash:
  1. b86a7517426286535761a14ca8504cb9
  2. b86a7517426286535761a14ca8504cb9
  3. b86a7517426286535761a14ca8504cb9

- Execution Time: 
  1. 5089 seconds
  2. 5081 seconds
  3. 5095 seconds

- Data Processed Per Second:
  1. 0.02515228925132639025 GB/s
  2. 0.02519189135996851013 GB/s
  3. 0.02512266928361138370 GB/s


### ***Unicage***

- Implementation: [boaSort.sh](../../../../../workloads/batch/sort/bashSort/boaSort/boaSort.sh)

- Output Hash:
  1. b86a7517426286535761a14ca8504cb9
  2. b86a7517426286535761a14ca8504cb9
  3. b86a7517426286535761a14ca8504cb9

- Execution Time: 
  1. 3171 seconds
  2. 3175 seconds
  3. 3277 seconds

- Data Processed Per Second:
  1. 0.04036581520025228634 GB/s
  2. 0.04031496062992125984 GB/s
  3. 0.03906011595971925541 GB/s


---
## Special Considerations:

TODO


---
## Conclusions:

TODO