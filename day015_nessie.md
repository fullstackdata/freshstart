# Nessie - Git for data
MLOps need data versioning for the models they were built for.
* Git-like experience for the Data Lake
  * Branches, tags, commits, merges
  * Tag - same as a branch, but <b>CANNOT BE COMMITTED to</b> 
* Scale-out and designed for FAAS (function as a service, AWS Lambda), Kubernetes, Docker
* Supports common data standards - Hive Tables, Iceberg, Delta Lake, SQL Views
*  !!! Multi-table Transactions !!!
*  Version control of <b>metadata</b>, not actual data
*  For MLOps, create a branch before starting model training, merge the branch after training
*  Good for reproducibility in MLOps with versioned data like above

##### DeltaLake vs Iceberg
* Iceberg - list of all files
* DeltaLake - tracking deltas

