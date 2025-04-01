
# Apache Kafka

## Introduction

Apache Kafka is a distributed event streaming platform designed for real-time data streaming, processing, and storage. Originally developed by LinkedIn, Kafka has become widely used for building scalable, fault-tolerant, and high-throughput data systems.

Kafka handles large volumes of real-time data feeds, enabling communication in microservices architectures, data pipelines, and event-driven applications.

## Key Concepts

### Topics

A topic is a logical channel for messages. Producers send messages to Kafka topics, and consumers read messages from them.

### Producers

A producer is an application or service that sends messages to Kafka topics. It can send data asynchronously to Kafka without having to wait for acknowledgment from consumers.

### Consumers

A consumer is an application or service that subscribes to topics and reads messages from them. Consumers can process data in real-time or in batch mode, depending on the use case.

###  Brokers

A broker is a Kafka server that stores and manages the messages. Kafka brokers handle message delivery, replication, and fault tolerance. Multiple brokers form a Kafka cluster that enables high availability and scalability.

### Partitions

Each topic in Kafka is divided into partitions. Partitions are used to split the data into smaller chunks and allow multiple consumers to read from different parts of the topic simultaneously. This helps scale Kafka and provides parallelism.

### Consumer Groups

A consumer group is a group of consumers that work together to consume messages from a topic. Each consumer in the group reads from a subset of partitions, ensuring that every message in the topic is processed by only one consumer in the group.

### Zookeeper

Zookeeper is used by Kafka for coordination and management of brokers in a Kafka cluster. It helps in leader election, maintaining metadata, and ensuring fault tolerance.

## How Kafka Works

### Data Flow in Kafka

#### Producer Sends Messages:
The producer sends messages to Kafka topics. Each message is written to a partition of the topic.

#### Messages Stored in Partitions:
Kafka stores messages in partitions. Each partition is an ordered, immutable sequence of messages.

#### Consumer Reads Messages:
Consumers subscribe to topics and consume messages from partitions. Each consumer keeps track of its position in the partition (called an offset) to know where to start reading next.

#### Replication:
Kafka replicates each partition to multiple brokers for fault tolerance. If one broker fails, another broker can take over.

### Kafka's Message Retention

Kafka retains messages for a configurable retention period. Once the retention period expires, the messages are deleted. This allows Kafka to manage large volumes of data while still providing historical access to data within the configured retention window.


## Conclusion

Apache Kafka is a distributed, highly scalable, and fault-tolerant event streaming platform that is widely used in modern applications. Its ability to handle high-throughput, real-time data streams makes it suitable for a variety of use cases, including real-time data pipelines, event-driven architectures, and log aggregation. By decoupling producers and consumers, Kafka enables efficient communication in microservices-based architectures, allowing for better scalability, fault tolerance, and high availability.

Kafka’s key features, such as message retention, replication, and partitioning, make it an ideal solution for building distributed, real-time applications that can handle large amounts of data.

## References

- Beginner Tutorials:

   https://www.youtube.com/watch?v=QkdkLdMBuL0

   https://www.youtube.com/watch?v=06iRM1Ghr1k

- Official Documentation:
   
    https://kafka.apache.org/documentation/

- Confluent: What is Apache Kafka?
   
  https://www.confluent.io/what-is-apache-kafka/





