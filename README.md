# simple-python-kafka
- producer: produces csv contents to a topic
- consumer: consumes csv contents

# kafka version+directory setting
- C:\kafka\kafka_2.13-2.7.0\bin\windows

# create topic
- .\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic hello
~~- bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --partitions 1 --replication-factor 1 --topic csvdata~~

# ~~list topic~~
~~- bin\windows\kafka-topics.bat --list --zookeeper localhost:2181~~

# producer
- .\kafka-console-producer.bat --broker-list localhost:9092 --topic hello

# consumer
- .\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic hello --from-beginning

# push messages (>, available @consumer cmd)
- .\kafka-console-producer.bat --broker-list localhost:9092 --topic hello

# push files
- .\kafka-console-producer.bat --broker-list localhost:9092 --topic hello < C:\Users\maeve\실습\Spark_temp\walmart_stock.csv
