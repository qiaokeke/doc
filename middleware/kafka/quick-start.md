* https://kafka.apache.org/quickstart
```
> tar -xzf kafka_2.12-2.2.0.tgz
> cd kafka_2.12-2.2.0

> bin/zookeeper-server-start.sh config/zookeeper.properties

> bin/kafka-server-start.sh config/server.properties

> bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test

> bin/kafka-topics.sh --list --bootstrap-server localhost:9092
test

> bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
This is a message
This is another message

> bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
This is a message
This is another message




```
