###### Zero Copy
Data transfer from one memory area to another is done without consuming CPU cycles.
Zero copy versions of OS elements such as network protocol stacks, file systems and device drivers efficiently utilize system resources.

###### Arrow Data as a service
###### Batch Streams
  * Flight = Multiple streams
  * Arrow Stream = Schema + Record Batches
  * Streams could be from different endpoints
###### Stream Management
  * Can handle backpressure??

Databricks ODBC driver has been optimized with reduced query latency and increased results transfer speed based on Apache Arrow serialization.

###### Pandas UDFs
Arrow is also used to exchange data directly between JVM and Python driver/executors with near zero ser/deser cost.
Deserialization is also automatically vectorized under the hood by Arrow.
