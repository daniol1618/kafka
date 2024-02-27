## Springboot Project to produce and consume data from/to topics.




# Instructions to Start a Kafka Cluster For testing Purposes

## Instructions

### Starting Zookeeper

1. Navigate to the Kafka installation directory.
2. Execute the following command to start Zookeeper:

```bash
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

### Starting Kafka Server
1. Navigate to the Kafka installation directory.
2. Execute the following command to start the Kafka server:

```bash
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

### Creating a Topic
1. Navigate to the Kafka installation directory.
2. Go to the /windows folder 
3. Execute the following command to create the topic:

```bash
kafka-topics.bat --create --bootstrap-server localhost:9092 --topic test
```

### Creating a Producer Console
1. Navigate to the Kafka installation directory.
2. Go to the /windows folder
3. Execute the following command to initialize the producer

```bash
kafka-console-producer.bat --broker-list localhost:9092 --topic test
```

### Creating a Consumer Console
1. Navigate to the Kafka installation directory.
2. Go to the /windows folder
3. Execute the following command to initialize the consumer

```bash
kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092 --from-beginning
```