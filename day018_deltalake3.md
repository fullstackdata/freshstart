MERGE INTO

    Reference - https://www.youtube.com/watch?v=7ewmcdrylsA
    Merge into is a process similar to inserting new records or updating existing records, but instead of a predicate, an entire source table (CDC) is merged into the target table.
    Two-pass scans are done to perform this action.
    Scan 1 - identify the files that need to be updated.
        Add more predicated to narrow down the search space
        z-order based on the query's keys and predicates.
        Adjust shuffle partitions
        Adjust broadcast thresholds
        Compact too many small files, but not too large files, 1GB per file is usually ideal.
    Scan 2 - rewrite the identified files
        Enable automatic re-partitioning, or optimized writes in Databricks DeltaLake.
        Full outer join does not support broadcast joins, right join can. 
    In addition to standard SQL syntax, there is extended SQL syntax to make this 'MERGE INTO' process more efficient.
    This extended SQL syntax provides multiple clause conditions to identify and filter only the relevant files, thus making the process efficient.
    DON'T CACHE the target table, can lead to cache coherency issues.
    Source table caching can speed up the second pass of scans.

 
