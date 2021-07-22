# Dremio Data Reflections

Traditional Datawarehouses had multiple copies of data in datamarts.
Datalakes made the problem worse by having unrefined, schema on read data.
Users have varied needs, they don't want to wait weeks or months for IT to make changes
Self-service is very important.

## Virtual Datasets
Logical or virtual datasets address the problem of data copies.
Physical copies have security risks as well as cost of storage, which don't happen if the copies are logical
Relational cache to address performance issues of computing logical datasets from physical datasets.

### Reflections 
Reflections shorten the distance to data.
All that's done through reflections is already done today, by using materialization, but manually.
They are not required on day 1, can be added at any time.
