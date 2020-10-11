# Kafka-JMX-Trans
Kafka Broker Monitoring using Jmxtrans-Agent


How to Setup Guide---

Add this line to Kafka Broker StartUp script
1. Download jmxtrans-agent-1.2.10.jar from https://github.com/jmxtrans/jmxtrans-agent/releases/tag/jmxtrans-agent-1.2.10
2. Add this line to kafka broker startup script
export KAFKA_OPTS="-javaagent:/path/to/jmxtrans-agent-1.2.10.jar=/path/to/kafka-jmxtrans-agent.xml"


Description---

1. kafka-jmxtrans-agent.xml is a configuration file for collecting kafka metrics using jmxtrans-agent and writting them in a file or sending them to graphite for graphana dashbopards 
2. kafka-object.yaml is the a yaml file consisting the list of metrics that kafka expose through jmx
3. kafkajmx-graphana.json is a json file for collecting essential metrics from graphite and making dashboard in graphana


Few Links --

Jmxtrans-Agent Github Repository
https://github.com/jmxtrans/jmxtrans-agent

Kafka Metrics MBeans List
http://kafka.apache.org/documentation.html#monitoring

Kafka Metrics Monitoring Basics
https://www.datadoghq.com/blog/monitoring-kafka-performance-metrics

Few important metrics in kafka
https://docs.confluent.io/current/kafka/monitoring.html