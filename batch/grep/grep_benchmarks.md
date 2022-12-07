# Grep Benchmark

## Benchmark Results:

---
### Data-set Volumes:

- [64 GB](grep-64GB/grep-64GB_benchmarks.md)
- [128 GB](grep-128GB/grep-128GB_benchmarks.md)
- [256 GB](grep-256GB/grep-256GB_benchmarks.md)
- [512 GB](grep-512GB/grep-512GB_benchmarks.md)
- [1024 GB](grep-1024GB/grep-1024GB_benchmarks.md)
- [2048 GB](grep-2048GB/grep-2048GB_benchmarks.md)
- [4096 GB](grep-4096GB/grep-4096GB_benchmarks.md)
- [8192 GB](grep-8192GB/grep-8192GB_benchmarks.md)


---
## Special Considerations:

- The implementation of Grep on Spark was adjusted for the 8192 GB benchmark, in order to fix a buffer overflow bug that was occurring. The fix simply changed the type of the counter from *int* to *long*.


---
## Conclusions:

Sparks's performance fell for the 8192 GB - RDD recomputing.

The Unicage implementation performed better than Hadoop and Spark for all experiments.
