# kafka-example
Simple example for reading and writing into Kafka. Elasticsearch-Flink still needs to be updated.


# Set up Kafka

```bash
# start zookeeper server
./bin/zookeeper-server-start.sh ./config/zookeeper.properties

# start broker
./bin/kafka-server-start.sh ./config/server.properties 

# create topic “test”
 ./bin/kafka-topics.sh --create --topic test --zookeeper localhost:2181 --partitions 1 --replication-factor 1

# consume from the topic using the console producer
./bin/kafka-console-consumer.sh --topic test --zookeeper localhost:2181

# produce something into the topic (write something and hit enter)
./bin/kafka-console-producer.sh --topic test --broker-list localhost:9092

#start flink
Open the app and start ReadToKafka and WriteIntoKafka with required arguments. 
```
