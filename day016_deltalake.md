# Delta Lake
* It is an open source table format, similar to Iceberg.
* While Iceberg has a snapshot of table files, Delta Lake has a list of deltas.
* Metadata needed for tables are colocated with data.
  * my_table
    * delta_log
      * 000000.json
      * 000001.json
    * date=2021-07-16
      * part_0001.parquet
      * part_0002.parquet   
* Data is in parquet format, metadata is in JSON format.
* Tables are optimistically locked for concurrent users since majority of usecases are new writes rather than updating the same data.
* For really big data, even metadata is big and is often a bottleneck. Delta tables use Spark to process metadata. 
* Checkpoints are created in parquet, once for every ten commits.
