# Unicage-Benchmarks

These are the results (metrics and execution logs) collected from big data benchmarks with terabyte-sized datasets generated with BDGS from BigDataBench and processed with Unicage, Hadoop, Hive and Spark. 

All cluster monitoring and benchmarked resource usage metric collection was achieved with Netdata. These have a total of +8GB, together with the logs of the benchmarks. The size of this archive warranted a separate repository. The code and further documentation of the benchmark is available in [this repository](https://github.com/duartegithub/Unicage-Benchmarks-2021-2022-Archive).

---
## Benchmark Results

---
### ***Batch processing***

- [grep](./batch/grep/grep_benchmarks.md)
- [sort](./batch/sort/sort_benchmarks.md)
- [wordcount](./batch/wordcount/wordcount_benchmarks.md)

---
### ***Query processing***

- [select](./query/select/select_benchmarks.md)
- [join](./query/join/join_benchmarks.md)
- [aggregation](./query/aggregation/aggregation_benchmarks.md)

---
## Notes:

- The notes under the *Special Considerations* and *Conclusions* sections of the documentation linked above are crude. Many of those notes devolved into meaningless details, others evolved into interesting conclusions. 

- The data-set volumes reported by PDGF in the logs of the generation of structured data are not trustworthy. The files called *genload_actual_volume* state the actual accurate volumes of the produced data-sets, in bytes.

- The *data processed per second* metric documented here are not trustworthy, as it simply divides the planned volumes of the data sets by the execution time, and doesn't consider the error in data generation, nor the partial size of the tables for the select and aggregation workloads. However, since this value tends to be rather linear, it is still fitting to visualize fluctuations in performance. For accurate depictions of these metrics, divide the Actual Sizes by the Execution Times