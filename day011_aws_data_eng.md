# Streaming Data Ingestion
* Realtime - Kinesis DataStreams
* Near RealTime - Kinesis Data Firehose
* Analytics on a Stream - Kinesis Analytics
* KDS -> KA -> KDS | KDF
* KDF -> KA -> KDS | KDF

# AWS Batch
* One job per EC2 instance by default
* Managed compute environment
  * Choice of On-Demand or Spot instances 
  * Set a maximum price for spot instances
  * Set min & max vCPU
* Triggered by CloudWatch Events
* Orchestration by AWS Step Functions
* Compared to Lambda, there is no runtime environment, time or memory limitation.  
* Run jobs as Docker images
* Unmanaged compute environment is possible too
* Multi node mode for HPC, works better with a <b>cluster</b> placement group

# EMR
* Hive can read from DynamoDB
* EMRFS - an implementation of HDFS for EMR to write directly to S3
