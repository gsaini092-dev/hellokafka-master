# hellokafka-master
 Kafka Producer-Consumer Example

## Download the Kafka kafka_2.12-3.0.0 binary
```
cd kafka_2.12-3.0.0
```
# For Mac OS

## Run the zookeeper & kafka server
```
./bin/zookeeper-server-start.sh config/zookeeper.properties
./bin/kafka-server-start.sh config/server.properties
```

## Create topics:
```
./bin/kafka-topics.sh --create --partitions 1 --replication-factor 1 --topic first-topic --bootstrap-server localhost:9092
```

## Create a producer, Here, 9092 is the port number of the Kafka server
```
./bin/kafka-console-producer.sh --topic first-topic --bootstrap-server localhost:9092
```

## Consumer
```
bin/kafka-console-consumer.sh --topic first-topic --from-beginning --bootstrap-server localhost:9092
```

==============================

## List kafka
bin/kafka-topics.sh --bootstrap-server localhost:2181 --list

## Describe partitions
bin/kafka-topics.sh --bootstrap-server localhost:2181 --describe

## Delete topics
bin/kafka-topics.sh --bootstrap-server localhost:2181 --topic myfirstTopic --delete


# For Windows Installation:
Step 1.
First need to Start Zoopkeepr & Kafka Server  ,
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
.\bin\windows\kafka-server-start.bat .\config\server.properties

Step 2.
Create your own Topic 

.\bin\windows\kafka-topics.bat --create --partitions 1 --replication-factor 1 –topic  first-topic --bootstrap-server localhost:9092


Step 3. For sperate CMD(create producer)

.\bin\windows\kafka-console-producer.bat --topic  first-topic --bootstrap-server localhost:9092

Step 4. For separate CMD(create consumer)
.\bin\windows\kafka-console-consumer.bat –topic first-topic --from-beginning --bootstrap-server localhost:9092

Then --------------------------Ready To USE KAFKA--------------------------------------


