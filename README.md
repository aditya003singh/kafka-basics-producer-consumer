# _Kafka-Basics-Producer-Consumer_
This project demonstrates basic Kafka producer and consumer functionality using Java. It explores various configuration properties and showcases how to send and receive messages with Kafka. Perfect for beginners looking to understand Kafka's core concepts and implementation.

## Topics Covered
The topics below cover the fundamental and advanced Kafka producer and consumer functionalities, including message handling, partitioning strategies, consumer group coordination, and efficient data processing techniques.

## Kafka Producer
#### Simple Kafka Producer Demo
Demonstrates the basics of writing messages to a Kafka topic. This simple example covers the essential steps to create a Kafka producer and send messages.

### Kafka Producer Demo with Callback
Explains the use of the callback interface to provide feedback on message delivery, including the partition and offset where each message was sent. Highlights the differences between the Round Robin partitioner, which can lead to inefficiencies by creating many small batches, and the StickyPartitioner, which improves efficiency by batching data to the same partition.

### Kafka Producer with Keys Demo
Illustrates how to use keys in Kafka producers to ensure that messages with the same key are sent to the same partition, maintaining order.

## Kafka Consumer
### Kafka Consumer Demo
Covers the basics of creating and configuring a Kafka consumer to receive data. Discusses delivery semantics, including the concepts of at-most-once, at-least-once, and exactly-once delivery guarantees.

### Kafka Consumer Demo with Graceful Shutdown
Shows how to implement a shutdown hook to gracefully close a Kafka consumer, ensuring that all resources are properly released and no data is lost during shutdown.

### Kafka Consumer Demo with Cooperative Rebalance
Explains the cooperative rebalancing strategy, which prevents consumers in a group from completely stopping message consumption when partitions or consumers are added or removed. This approach ensures a smoother and more efficient rebalancing process.

## Advanced Kafka Consumer Topics
### Kafka Consumer Rebalance Listener
Demonstrates how to use a ConsumerRebalanceListener to manage partition reassignments. A common use case is saving offsets in a custom store, ensuring that offsets are saved during the onPartitionsRevoked(Collection) call whenever partition assignments change.

### Kafka Consumer Seek and Assign
Explains how to use the seek and assign methods to read specific messages from specific partitions, allowing for fine-grained control over message consumption.

### Kafka Consumer in Threads
Discusses the benefits of running a Kafka consumer in a separate thread, allowing the main thread to perform other tasks concurrently. This setup can improve application performance and responsiveness.