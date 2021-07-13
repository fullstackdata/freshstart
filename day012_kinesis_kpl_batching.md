# Kinesis Producers

### Kinesis SDK 
  * Simple
  * Synchronous
  * PutRecords can be batched, increases throughput
  * ProvisionedThroughputExceeded
    * Hot shard (bad partition)
    * Retries with backoff
    * Increase shards
  
 ### Kinesis Producer Library
  * High performance, long running producers
  * Automated and configurable retry mechanism
  * Synchronous or asynchronous API (async for better performance)
  * Batching 
    * Collect - sending multiple records in one PutRecord call
    * Aggregate - multiple records in one record 
    * Introduces delay upto RecordMaxBufferedTime
  * Needs KCL to use deaggregation
    
 ### Kinesis Agent 
  * Built on top of KPL
  * Preprocess before sending to streams (csv to json, single line to csv etc)
  * Routing feature based on directory/log file
  * Metrics to CloudWatch for monitoring
  
    
