# DeltaLake
Enterprises want to make use of all kinds of data available without having to slow down to design data collection systems.
This has led to datalakes where raw data is collected without schema, commonly known as schema-on-read pattern.
Most columns are read as nullable, string columns rather than the appropriate data type like date or numeric types.

Individual teams refine data in this raw zone, add schema, cleanup, transformations as well as enrichments.
To reuse the work of a team by other teams in the enterprise, this intermediate data can be saved in bronze and silver zones.
Teams can build up on this and make the data pristine for their usage and write them to datawarehouse or use them for BI applications.

This pattern of collecting raw data and marking it as bronze, silver or gold based on the quality, transformations and aggregations is called the medallion architecture.
