### Heka Agent

[Heka](https://hekad.readthedocs.io/en/v0.10.0/) is an open source stream processing software system developed by Mozilla. Heka is a “Swiss Army Knife” type tool for data processing, useful for a wide variety of different tasks, such as:

 * Loading and parsing log files from a file system.
 * Accepting statsd type metrics data for aggregation and forwarding to upstream time series data stores such as graphite or InfluxDB.
 * Launching external processes to gather operational data from the local system.
 * Performing real time analysis, graphing, and anomaly detection on any data flowing through the Heka pipeline.
 * Shipping data from one location to another via the use of an external transport (such as AMQP) or directly (via TCP).
 * Delivering processed data to one or more persistent data stores.

This catalog entry is implementing a heka agent running on each host, gathering events via Docker socket and sending to a cluster of Kafka servers (for consumption of Heka Server).

Heka agent & Heka server are somehow inappropiate names for hekad daemon running with different configurations of input, output and other plugins.
