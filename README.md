# BD1_484_496_500_506
Repo created programmatically. Project Title: Yet another Kafka (YaK)
YAK project developed as part of the final Big Data Project as required by the course Big Data (UE20CS322).
Developed by: Vijit Kumar, Vishakha Hegde, Vibhav Deepak and Vanshika Goel.

# Basic Structure and Working
## MINI ZOOKEEPER:
- in case of failure, elect new leader (heartbeat, polling)
- zookeeper is always running, never fails

## KAFKA BROKERS: (3)
- create and manage topics
- if topic doesnt exist, create one
- topics stored as directories in file system
- partition the topics
- register/de-register producers and consumers
- keep track of which messages have reached a particular consumer
- publish operations: only leader
- consume operations: leader or replicas
- leader maintains log of operations--replicated on followers too
- handle situations where publish/consume happens when leader dies (eg retry in x amt of time i.e after new leader is elected)

## KAFKA PRODUCER: (dynamic)
- publish messages to topic
- register to any topic/notify broker to create one
- get ack from broker when broker receives message, else re-transmit.

## KAFKA CONSUMER: (dynamic)
- receive messages from topic
- register to any topic/notify broker to create one
- receive all messages from start of topic (from-beginning flag)
- send ack to broker on receiving message

## KAFKA ZOOKEEPER
- Producer requests zookeeper for port of leader-->5566
- Consumer asks zookeeper which broker to take data from based on load


- Messages sent in form of JSON key-value pairs, Topics stored as directories in a file system.


