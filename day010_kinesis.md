# Kinesis Data Streams
* Real time streaming
* Shards are provisioned
* 1MB/s or 1000 messages per second per shard
* Data is automatically replicated synchronously to 3 AZ
* Three ways to produce
  * Simple SDK
  * KPL
  * Kinsesis Agent

## Kinesis Data Consumer
* Standard
  * 5 requests per second, 2MB/s per shard
  * Pull model
* Enhanced Fan Out
 * Clients register with KDS
 * EFO pipe per consumer
 * Push model

### Lambda Client
* Lambda process pulls a certain number of messages from the stream.
* If there is an error on one record, there is no way to checkpoint, this batch is retried indefinitely.
* To deal with these poison messages, capture and log the exceptions.
* Register lambda consumer as an Enhanced Fan Out consumer
*

# Kinesis 
