# Bigdata final exam

## 5. Twitter & Kafka & HBase

- Stream from twitter to Kafka producer. Track the keyword “COVID”
- Create a consumer the data and put into HBASE with fields: text, created by, date

You can get more description about this work in [Medium](https://medium.com/@jampttws/streaming-twitter-data-to-kafka-producer-and-publish-in-hbase-3d59ff9dcfaf)

## How to run instructions.

- Start server and zookeeper for Kafka

```
login hadoop.
$ cd kafka

start zookeeper.
$ bin/zookeeper-server-start.sh config/zookeeper.properties

start Kafka server.
$ bin/kafka-server-start.sh config/server.properties
```

- Start HBase
```
login hadoop.
$ cd hbase

start hbase.
$ bin/start-hbase.sh

start Thrift on port 9090.
$ bin/hbase-daemon.sh start thrift -p 9090
```

- Open jupyter notebook at https://localhost:8887

```
login your Hadoop and run jupyter notebook.
$ jupyter notebook --no-browser --port=8887

run server in the terminal.
$ ssh -N -L 8887:localhost:8887 user01@10.3.133.108

```

## Installation details
```
$ pip3 install kafka-python

$ pip3 install tweepy

$ pip3 install happybase

```

### Requirement
```
hbase_1.4.13
kafka_2.11-2.4.1
python > 3.6
```


## Author
Tanasorn Tritawisup  #6010545790