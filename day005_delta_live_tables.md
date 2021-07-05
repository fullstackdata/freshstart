# Delta Live Tables
* Automate a pipeline around a query
* Cluster creation included as well

###### Options for data ingestion into lakehouse 
* Partner integration network
* Simple SQL Copy Command
* Autoloader

#### Steps

###### Notebook
* Create a live table
* Add data quality constraints or expectations
* Drop rows that don't meet these expectations
* Option to carry on with good data or stop processing the whole dataset
* tblproperties
  * option to add it to a catalog for data discovery
  * optimization like zorder

###### Jobs Tab
* Create a pipeline.
* Pipeline is a DAG (directed acyclic graph) of data flow.
* Event details of a pipeline show the count of records that have been processed or the count of records that have failed validation.
* Event log can be queried. 
* Reports or dashboards can be created to show the status of these pipelines.
* Orchestration is possible to trigger other jobs to run an end to end workflow
