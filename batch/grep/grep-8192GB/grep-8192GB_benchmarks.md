# Grep Benchmarks: 8192 GB

---
## Benchmark Results:

- Data-set Actual Size:
  1. 8019.19 GB (used in the data processing benchmarks below)
  2. 8018.54 GB (wordcount)
  3. 8018.60 GB (grep-extra)

- Generation Time:
  1. 47573 seconds
  2. 45694 seconds (wordcount)
  3. 45618 seconds (grep-extra)

- Loading Time (HDFS):
  1. 10780 seconds
  2. 10704 seconds (wordcount)
  3. 10916 seconds (grep-extra)

- Loading Time (Unicage):
  1. 14843 seconds
  2. 12705 seconds (wordcount)
  3. 12632 seconds (grep-extra)


### ***Hadoop***

- Implementation: [hadoop-mapreduce-examples-3.3.1.jar](../../../../../workloads/batch/grep/javaGrep/hadoop-mapreduce-examples-3.3.1.jar)

- Output Hash:
  1. b4aa7bacec5c1df231bb61cf0315bef8
  2. b4aa7bacec5c1df231bb61cf0315bef8
  3. b4aa7bacec5c1df231bb61cf0315bef8

- Execution Time: 
  1. 24003 seconds
  2. 24066 seconds
  3. 24104 seconds

- Data Processed Per Second:
  1. 0.34129067199933341665 GB/s
  2. 0.34039724092080113022 GB/s
  3. 0.33986060404912047792 GB/s


### ***Spark***

- Implementation: [Grep.scala (fixed)](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow))

- Output Hash:
  1. b4aa7bacec5c1df231bb61cf0315bef8
  2. b4aa7bacec5c1df231bb61cf0315bef8
  3. b4aa7bacec5c1df231bb61cf0315bef8

- Execution Time: 
  1. 19057 seconds
  2. 18719 seconds
  3. 18357 seconds

- Data Processed Per Second:
  1. 0.42986828986724038411 GB/s
  2. 0.43763021528927827341 GB/s
  3. 0.44626028218118428937 GB/s


### ***Unicage***

- Implementation: [tukubaiGrep_parallel_fifo.sh](../../../../../workloads/batch/grep/bashGrep/tukubaiGrep_parallel_fifo.sh)

- Output Hash:
  1. b4aa7bacec5c1df231bb61cf0315bef8
  2. b4aa7bacec5c1df231bb61cf0315bef8
  3. b4aa7bacec5c1df231bb61cf0315bef8

- Execution Time: 
  1. 8576 seconds
  2. 8591 seconds
  3. 8575 seconds

- Data Processed Per Second:
  1. 0.95522388059701492537 GB/s
  2. 0.95355604702595739727 GB/s
  3. 0.95533527696793002915 GB/s


---
## Special Considerations:

- Spark's nohup.out (log) is compressed with `tar cfz nohup.out.tgz nohup.out`, uncompress with `tar zxvf nohup.out.tgz`.

- The output of Spark for the grep workload on the 8192 GB data-set was in disagreement with both Unicage and Hadoop. Spark reached the same result across all three runs, but this output was a negative number, which does not make sense in the context of a grep output and for this reason, the output of Spark is certainly wrong.

  > **EDIT:** It has been discovered that this bug was due to a buffer overflow that happened because the counter was implemented as an Integer in the [original implementation](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala%20(buffer%20overflow)). The [fixed implementation](../../../../../workloads/batch/grep/scalaGrep/src/main/scala/Grep.scala) changes the counter type to Long and produces the correct results. The Spark results reported in this document reflect 3 runs of the fixed implementation.


---
## Conclusions:

TODO


