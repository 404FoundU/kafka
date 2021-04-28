# kafka

https://www.youtube.com/watch?v=R873BlNVUB4&t=3s

docker run --name zookeeper -p 2181:2181 zookeeper

docker run --name kafka3 -p 9092:9092 -e KAFKA_ZOOKEEPER_CONNECT=localhost:2181 -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:9092 -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 confluentinc/cp-kafka


docker run --net=host --name=zookeeper -e ZOOKEEPER_CLIENT_PORT=32181 -e ZOOKEEPER_TICK_TIME=2000 -e ZOOKEEPER_SYNC_LIMIT=2 confluentinc/cp-zookeeper:6.1.1

docker run -d  --net=host  --name=kafka  -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:32181  -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:29092  -e KAFKA_BROKER_ID=2  -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1  confluentinc/cp-kafka:6.1.1


docker run   --net=host  --name=zookeeper  -e ZOOKEEPER_CLIENT_PORT=2181  confluentinc/cp-zookeeper:5.0.0

docker run   --net=host  --name=kafka  -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181  -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://kafka:9092  -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1  confluentinc/cp-kafka:5.0.0



docker run -d --net=host --name=zookeeper -e ZOOKEEPER_CLIENT_PORT=32181 -e ZOOKEEPER_TICK_TIME=2000 -e ZOOKEEPER_SYNC_LIMIT=2 confluentinc/cp-zookeeper:6.1.1

docker run -d  --net=host  --name=kafka  -e KAFKA_ZOOKEEPER_CONNECT=localhost:32181  -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:29092  -e KAFKA_BROKER_ID=2  -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1  confluentinc/cp-kafka:6.1.1


docker run -p 9092:9092 --name kafka  -e KAFKA_ZOOKEEPER_CONNECT=localhost:2181 -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:9092 -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 -d confluentinc/cp-kafka


https://kafka.js.org/docs/getting-started