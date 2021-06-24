# Photon Engine 
Native execution engine on Databricks

[Photon Technical Deep Dive](https://www.youtube.com/watch?v=pNn5W4ujP3w)

## Motivation
  #### Hardware Improvements
  * In the past ten years, there have been tremendous improvements in network and disk access speeds.
  * CPU is now the new bottleneck.
  * Necessitates squeezing out as much of the CPU power as possible.
  #### Changing nature of workloads
  * Popularity of data lakes and the value they provide to data driven organizations create different types of workloads
  * In a <b>medallion architecture</b> (raw -> bronze -> silver -> gold) query execution for raw data is different than query execution for pristine data.
    * In the raw zone, to collect as much data as possible, schemas are not defined. 
    * Every field is treated as a string.
    * Not null constraints are not defined.
    * Query execution that includes data type casting or null checking adds delays to query time.

## Solution
  * Decompose query into compute kernels that process vectors.
  * Take advantage of CPU's batch processing capabilities like SIMD.
  * Runtime adaptivity - batch level specialization like NULLs or no NULLs.
  * Microbenchmark speed up 5X-60X.
  * Expression evaluation - 30% slower for null checking.
  * Comparison in filters, replacing value with a lit makes it 25% faster.
  * Lazy representation - avoid eager evaluations and mark records as active rows for further processing
  
## Real world performance
  * Best speedup - 16X
  * Typical - 2-3X end-to-end
