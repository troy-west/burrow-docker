# docker-burrow

Docker compose file supporting Burrow and Burrow Dashboard in the same network

# run

Four required environment variables:
1. KAFKA_VERSION= the version of Kafka you are using in your cluster
2. KAFKA_BROKERS= a comma seperated list of the host and port ("host:port") of your Kafka brokers
3. ZOOKEEPER_SERVERS= a comma seperated list of the host and port ("host:port") of your Zookeeper servers, in quotes
4. ZOOKEEPER_PATH= a full path to the znode that Burrow is allow to write under, in quotes. The path will be created if it does not already exist.

e.g.

``` shell
KAFKA_VERSION=1.0.0 KAFKA_BROKERS=\"localhost:9092\" ZOOKEEPER_SERVERS=\"localhost:2181\" ZOOKEEPER_PATH=\"/gw-kafka\" docker-compose up
```

# behold

Burrow @ http://localhost:8000
Burrow Dashboard @ http://localhost:8080
