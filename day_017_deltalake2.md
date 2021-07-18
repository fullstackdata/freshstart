

Since a transaction log file has the path (S3 location in AWS) saved in it, this leads to a better performance. This is the default behavior.

 

For data compaction process of too many small files, set dataChange to false, since this is just a rearrangement of existing data, not any change in data.

 

When doing 'MERGE INTO' there is no need to specify all conditions. If the use case is just to add new data, use WHEN NOT MATCHED, no need to specify WHEN MATCHED.

 

Vacuum on a schedule (usually once a week) during off-peak hours.

 

Delta Lake allows concurrent multiple reads or multiple writes due to isolation and serializability provided by the transaction log.

 

For schema evolution, schema change (data type change) possible only for certain data types. Ensure the changes are parquet compatible.

Delta lake under the hood creates an additional empty checkpoint just for the change of schema. New data is indicated in the subsequent transaction log file.

A schema is mandatory in Delta Lake.

Choose mergeSchema=True for evolution.

When there is a 'mergeSchema', no changes are needed to existing data. New columns with null values are added when old data is read, no performance issues since old data is not changed during writes.

For incompatible changes, overwriteSchema should be used. Old data needs to be rewritten.

Schema enforcement is transactional - either entire table or dataframe is written or is rejected. No need to keep track of individual records.

When data write fails due to schema enforcement, exceptions are raised.

No automatic replays, just exceptions to notify of the schema/data incompatibility.

For SCD Type 2, use md5() function to generate the surrogate key. This requires the change of the key type from an Integer to a String.
