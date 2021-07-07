# Arrow
* An on-the-wire columnar format, which means there is no need and overhead of serialization and deserialization.
* A batch of rows are transferred at a time - <b>Record Batch</b>.
* <b>Data streams</b> - sequences of Arrow record batches.


# Flight
* gRPC messaging libraries typically used for microservices
* Enhancements to gRPC messaging libraries for data streams of large datasets
* Client-Server architecture
* Server serves <b>flight of data</b> requests from clients
* Supports encryption and authentication out of the box using gRPC's built in TLS, OpenSSL capabilities.
* No bottleneck of data access through a coordinator.
* Distributed data access is horizontally scalable, direct from data nodes.

# Applications
* Dremio's flight-based connector delivers 20-50X performance improvements over ODBC.
