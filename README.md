# Avro SpringBoot Starter для работы с Apache Kafka

### запустить Docker демона
```
sudo service docker start
sudo service docker stop
```

### получить свой ip
```
hostname -I
```

### запустить Kafka в docker (и Zookeeper)
```
docker-compose up -d
```

### зайти в контейнер и проверить топики
```
docker exec -it kafka bash
kafka-topics --create --topic rest_data --bootstrap-server localhost:9092
kafka-topics --list --bootstrap-server localhost:9092
```

### вывести лог топика
```
kafka-console-consumer --bootstrap-server localhost:9092 \
--topic rest_data \
--from-beginning
```

```
Avro — это система сериализации (превращение объектов в массив байтов) данных, которая используется для работы с объектами в потоковой (распределенной) среде. Avro является кроссплатформенной (не зависит от операционной системы и вида аппаратных ресурсов) системой, которая не зависит от языка программирования. Авро использует систему, основанную на схемах входных данных. Схемы могут включать в себя тип данных, структуру данных, формат записи данных, а также параметры их передачи (например, URL, порт и т.д.). Схемы Avro описываются c помощью JSON-формата (JavaScript Object Notation), что обеспечивает Авро независимость от языковой реализации. Для работы с Kafka используется специальный реестр схем (Schema Registry), который хранит в себе все схемы записей, использующихся брокером в данный момент времени.
```