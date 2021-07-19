# kafka-docker-container
This is docker compose file for installing Kafka and Zookeeper

This provides the default ports of Zookeeper and Kafka to external world.

Just for additional information how to create, send and consume messages on that simple setup.

- docker-compose up -d to setup project
- Next commands should be executed on the kafka container, so first log in into the container by typing:
- docker-compose exec kafka bash to enter kafka`
/bin/kafka-topics --create --topic topic-name --bootstrap-server localhost:9092 - will create topic
/bin/kafka-console-consumer --topic topic-name --from-beginning --bootstrap-server localhost:9092 <-- will execute consumer on topic-name topic
In new terminal on kafka container type /bin/kafka-console-producer --topic topic-name --bootstrap-server localhost:9092 <--- and now You can type messages that will be listening in You consumer

