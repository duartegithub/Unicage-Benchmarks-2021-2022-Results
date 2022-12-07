# Aggregation Benchmarks: 512 GB

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

- Implementation: [e-commerce-aggregation.sql](../../../../../workloads/query/interactive/SQLQuery/e-commerce-aggregation.sql)

- Output Hash:
  1. c84ca715fa78a6a0d0435c3e33047a8f
  2. c84ca715fa78a6a0d0435c3e33047a8f
  3. c84ca715fa78a6a0d0435c3e33047a8f

- Execution Time: 
  1. 3758 seconds
  2. 3930 seconds
  3. 3912 seconds

- Data Processed Per Second:
  1. 0.13624268227780734433 GB/s
  2. 0.13027989821882951653 GB/s
  3. 0.13087934560327198364 GB/s


### ***Spark***

- Implementation: [Aggregation.scala](../../../../../workloads/query/interactive/scalaQuery/src/main/scala/Aggregation.scala)

- Output Hash:
  1. c84ca715fa78a6a0d0435c3e33047a8f
  2. c84ca715fa78a6a0d0435c3e33047a8f
  3. c84ca715fa78a6a0d0435c3e33047a8f

- Execution Time: 
  1. 695 seconds
  2. 705 seconds
  3. 708 seconds

- Data Processed Per Second:
  1. 0.73669064748201438848 GB/s
  2. 0.72624113475177304964 GB/s
  3. 0.72316384180790960451 GB/s


### ***Unicage***

- Implementation: [boaAggregationV3.sh](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregationV3.sh)

- Output Hash:
  1. c84ca715fa78a6a0d0435c3e33047a8f
  2. c84ca715fa78a6a0d0435c3e33047a8f
  3. c84ca715fa78a6a0d0435c3e33047a8f

- Execution Time: 
  1. 930 seconds
  2. 926 seconds
  3. 926 seconds

- Data Processed Per Second:
  1. 0.55053763440860215053 GB/s
  2. 0.55291576673866090712 GB/s
  3. 0.55291576673866090712 GB/s


---
## Special Considerations:

- The data generation and loading for the query processing experiments makes it so the volume of the input data-set directly affects the size of each input file, but the number of input files remains the same. 

  The aggregation output for a 512 GB input data-set of Unicage was in disagreement with those of Hive and Spark. As an intermediate step, the implementation with Unicage has to sort the input data-set in order to perform the aggregation. 
  
  As the input files grow in size with the volume of the input data-set, and in the [original Unicage implementation](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregation.sh), this intermediate sort failed and caused the workload to output wrong results. So, in order to complete the aggregation workload for a 512 GB data-set, an [alternative Unicage implementation](../../../../../workloads/query/interactive/bashQuery/aggregation/boaAggregation/boaAggregationV3.sh) had to be used, and the results in this document reflect 3 runs of said alternative implementation. There was a performance impact.


---
## Conclusions:

TODO