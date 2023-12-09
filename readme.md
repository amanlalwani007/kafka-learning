# Learning kafka Ref :- https://youtu.be/ei6fK9StzMM?si=9xFuRu9yQrAOSNad
## apache kafka is like a communication system that helps different parts of a computer system exchange data by publishing and subscribing to topics.
# Usages :- 
1. OLA driver location update 
2. zomato live  food tracking 
3. Notification system to huge user . 




installing kafka 
Dwonload kafka zip file 
extract file
you will all sh files inside bin 
start zookeeper 
➜  kafka-3.6.1-src ./bin/zookeeper-server-start.sh config/zookeeper.properties
➜  kafka_2.13-3.6.1 ./bin/kafka-server-start.sh config/server.properties

Console commands 
1. create new topic with kafka topics 
2. produce example message with kafka-console-producer
3. consume the message with kafka-console consumer.

Command 1 :- Create a topic 
➜  bin ./kafka-topics.sh --create --topic user-topic --bootstrap-server localhost:9092
Created topic user-topic.

Command 2: produce data into topic
➜  bin ./kafka-console-producer.sh --topic user-topic --bootstrap-server localhost:9092
>hi
>this is my message
>consume it

Command 3: Consumer data from topic
➜  bin ./kafka-console-consumer.sh  --topic user-topic --from-beginning --bootstrap-server localhost:9092
hi
this is my message
consume it