# Kafka Topic

In Apache Kafka, a topic is a category or feed name to which messages are published. A topic in Kafka is similar to a table in a database or a folder in a file system. It's a logical container that holds a stream of records, where each record is a key-value pair.

![](https://kafka.apache.org/images/streams-and-tables-p1_p4.png align="left")

**When a producer sends a message to Kafka, it specifies the name of the topic to which the message should be published. Kafka then stores the message in the topic partition, which is a subset of the topic that is stored on a broker.**

Multiple producers and consumers can write and read data from the same topic. This allows for the decoupling of data producers and data consumers, making it possible to build highly scalable and distributed systems.

Topics in Kafka can be partitioned to enable parallel processing of data. Each partition is an ordered and immutable sequence of records. By partitioning a topic, the Kafka cluster can distribute the load across multiple brokers and process a large amount of data in parallel.

Topics can also be replicated across multiple brokers to provide fault tolerance and high availability. This means that if a broker fails, the replicas of the topic partitions can be used to continue serving data.

Overall, Kafka topics provide a flexible and scalable way to organize and process data in real time. They are a fundamental building block of the Kafka messaging system and play a critical role in enabling the creation of real-time data pipelines and streaming applications.