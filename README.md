# kafka

1. To check the status of Kafka brokers in the cluster, you can use the `kafka-broker-api-versions.sh` script with the `--bootstrap-server` option to connect to one of the brokers and get the list of supported API versions:

```
kafka-broker-api-versions.sh --bootstrap-server kafka-headless:9092
```

2. To check the status of Kafka topics and their partitions, you can use the `kafka-topics.sh` script with the `--bootstrap-server` option and the `--describe` option to display detailed information about each topic and partition:

```
kafka-topics.sh --bootstrap-server kafka-headless:9092 --describe
```

3. To check the status of Kafka ZooKeeper, you can use the `zkCli.sh` script with the `-server` option to connect to the ZooKeeper service and get the status of the ZooKeeper ensemble:

```
zkCli.sh -server kafka-zookeeper-headless:2181
```

4. To list all the topics in your Kafka cluster, you can use the `--bootstrap-server` option 

```
kafka-topics.sh --bootstrap-server <Kafka-Bootstrap-Server-URL> --list
// example
// kafka-topics.sh --bootstrap-server sd-core-kafka-headless:9092 --list
```

5. To check the number of partitions for a particular topic in your Kafka cluster, you can use the `kafka-topics.sh` script with the `--describe` option.

```
kafka-topics.sh --bootstrap-server kafka-headless:9092 --describe --topic <topic>
```

`
