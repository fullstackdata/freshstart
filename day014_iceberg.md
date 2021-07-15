# Apache Iceberg
Hive Metastore format has wide adoption and works with almost any query engine, tool or framework.
However, efficiently pruning data from partitions is difficult with Hive Metastores.
HMS also has state in two places, the metastore and in a filesystem.
This makes it difficult for atomicity.

Iceberg is an open source <b>SCALABLE table format</b>
* with a lot of best practices built in
* enables efficient partition pruning
* inplace evolution for schema and layout?

##### Key Idea
Track all files in a table.
A snapshot is a complete list of files in a table.
Writers optimistically create new snapshots and then commit.


Data engineers do not usually want to tweak the performance of queries.
Iceberg is a format to make this automatic.

Replaced a multimillion dollar elasticsearch cluster!!!



###### Reference - https://www.youtube.com/watch?v=mf8Hb0coI6o
