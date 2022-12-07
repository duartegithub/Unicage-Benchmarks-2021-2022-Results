# Sort Benchmark

## Benchmark Results:

---
### Data-set Volumes:

- [64 GB](sort-64GB/sort-64GB_benchmarks.md)
- [128 GB](sort-128GB/sort-128GB_benchmarks.md)
- [256 GB](sort-256GB/sort-256GB_benchmarks.md)
- [512 GB](sort-512GB/sort-512GB_benchmarks.md)
- [1024 GB](sort-1024GB/sort-1024GB_benchmarks.md)
- [2048 GB](sort-2048GB/sort-2048GB_benchmarks.md)
- [4096 GB](sort-4096GB/sort-4096GB_benchmarks.md)
- [8192 GB](sort-8192GB/sort-8192GB_benchmarks.md)


---
## Special Considerations:

TODO


---
## Conclusions:

The sort benchmarks were not performed for input data-sets larger than 501 GB for two reasons. First, if the processing rate of Hadoop remains consistent, the execution time of sorting 512 GB with Hadoop is predicted to widely exceed the imposed 18 hours limit. Second, there were technical difficulties associated with the Unicage sort implementation.

We know that even if the Unicage implementation was able to produce correct outputs for larger input data-sets, it would not be able to complete the sort workload for input data-sets larger than 1024 GB. The sort workload produces an output equally as large as the input data-set, and the Unicage implementation had the limitation of having to consolidate this output in the Unicage leader node, which only had 1024 GB available for output storage. For Hadoop and Spark, the consolidation of the sorted output is abstracted by HDFS.

The sort benchmarks for the 1024 GB, 2048 GB, 4096 GB and 8192 GB input data-sets were not performed.
