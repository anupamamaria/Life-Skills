
# Apache Kafka

## Introduction

Apache Kafka, in simple terms, is a message broker that facilitates communication between services, but it is much more than that. It is a distributed event streaming platform designed for real-time data streaming, processing, and storage. 

Kafka handles large volumes of real-time data feeds, enabling communication in microservices architectures, data pipelines, and event-driven applications.

## Key Concepts

### Topics

A topic is a logical channel for messages. Producers send messages to Kafka topics, and consumers read messages from them.

### Producers

A producer is an application that sends messages to Kafka topics. Kafka allows sending data in an asynchronous manner for consumers.

### Consumers

A consumer is an application that subscribes to topics and reads messages from them. Consumers can consume data in real-time or in batch mode, based on the use case.

###  Brokers

A broker is a Kafka server that stores and manages the messages. Kafka brokers handle message delivery, replication, and fault tolerance.

### Partitions

Each topic in Kafka is divided into partitions. Partitions are used to split the data into smaller chunks and allow multiple consumers to read from different parts of the topic simultaneously. This helps scale Kafka and provides parallelism.

### Consumer Groups

A consumer group is a group of consumers that work together to consume messages from a topic. Each consumer in the group reads from a subset of partitions.This ensures that every message in the topic is processed by only one consumer in the group.

## How Kafka Works

### Data Flow in Kafka

#### Producer Sends Messages:
The producer publishes messages to Kafka topics. Each message is written to a partition of the topic.

#### Messages Stored in Partitions:
Kafka stores messages in partitions. Partitions are ordered, immutable sequence of messages.

#### Consumer Reads Messages:
Topics are subscribed by consumers and messages are accessed from partitions. Each consumer maintains its position within the partition (called an offset) to know where to start reading next.

#### Replication:
Kafka replicates each partition to multiple brokers for fault tolerance. If one broker fails, another broker can take over.

### Kafka's Message Retention

Messages in Kafka are retained for a configurable retention duration. Once the retention period is up, the messages are deleted. This allows Kafka to manage large volumes of data while still making historical data available within the configured retention window.


## Conclusion

Apache Kafka is an extremely popular distributed, highly scalable, fault-tolerant event streaming platform used in modern applications. The streaming nature of user data supported by its high throughput and low latency makes it fit for many use cases like real-time data pipelines, event-driven architectures, log aggregation. Kafka is a messaging platform where producers and consumers are decoupled and it is engineered for efficient communication in microservices based architectures.

## References

- Beginner Tutorials:

   https://www.youtube.com/watch?v=QkdkLdMBuL0

   https://www.youtube.com/watch?v=06iRM1Ghr1k

- Official Documentation:
   
    https://kafka.apache.org/documentation/

- Confluent: What is Apache Kafka?
   
  https://www.confluent.io/what-is-apache-kafka/




