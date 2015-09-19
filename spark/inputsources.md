- Spark Streaming can receive streaming input from following services:

  |Source   |	Artifact                          |
  |---------|-----------------------------------|
  |Kafka    |	spark-streaming-kafka_2.10        |
  |Flume    |	spark-streaming-flume_2.10        |
  |Kinesis  | spark-streaming-kinesis-asl_2.10  |
  |Twitter  |	spark-streaming-twitter_2.10      |
  |ZeroMQ   |	spark-streaming-zeromq_2.10       |
  |MQTT     |	spark-streaming-mqtt_2.10         |

- Apart from the above mentioned services, spark can also accept streaming data from TCP ports directly.
- There might be some other ways to interact with spark. For e.g, if we are not concerned about stream processing of data, we can always dump data into HDFS or text files that spark can directly read. There are connectors available for Cassandra, S3, HDFS.

## Language Support:
1. Scala
