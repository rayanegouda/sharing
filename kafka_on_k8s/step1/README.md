
# DOCKER COMPOSE FOR KAFKA

The goal is to make a docker composed of kafka. It will be used for the rest of the project.
It is inspired by the Kafka docker bitnami on this link: https://hub.docker.com/r/bitnami/kafka

## Demo

Insert gif or link to demo
1- Lancer le cluster sur un terminal
docker compose -f ./step1/docker-compose.yaml up -d

2-Checker les logs sur un autre terminal

3- Se connecter au cluster

4- Afficher la liste des topics

5- Créer  un topic "mytopic" avec 3 partitions et replication 3
/opt/bitnami/kafka/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --topic mytopic --partitions 3 --replication-factor 3
/opt/bitnami/kafka/bin/kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic mytopic

6- Produire des messages en ligne de commande
kafka-console-producer.sh --bootstrap-server 127.0.0.1:9093 --topic mytopic

7- Consommer des messages en ligne de commande
kafka-console-consumer.sh --bootstrap-server 127.0.0.1:9093 --topic mytopic --from-beginning

8-Supprimer le topic

A checker : https://github.com/bitnami/containers/blob/main/bitnami/kafka/README.md
## Authors

- [@rayanegouda](https://www.github.com/rayanegouda)

