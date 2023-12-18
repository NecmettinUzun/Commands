# Topic Operation
## Update Topic partition count
> ./kafka-topics.sh --zookeeper localhost:2181 --alter --topic my-topic --partitions 20

## Describe Topic
> ./kafka-topics.sh --describe --zookeeper localhost:2181 --topic my-topic

## List Topic
> ./kafka-topics.sh --list --zookeeper localhost:2181

## Create Topic
> ./kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 13 --topic my-topic
