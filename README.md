# kafka-ecosystem

This repo contains a `docker-compose.yml` file to spawn a Kafka cluster with all its ecosystem.

## Usage

```bash
docker-compose up
```

## Components

### Zookeeper

Available on port 2181

### Kafka

a 3 Brokers cluster listening on ports 9092-9094

### Kafdrop

Exposes a web UI on [localhost:9000](localhost:9000) to view and manage cluster and topics

### ksqldb-server + ksqldb-client

To process and query streams.
CLI is available by running:

```bash
docker-compose exec ksqldb-cli ksql
```

### Schema Registry + UI

To register and use AVRO schemas.
The UI is available on [localhost:8000](localhost:8000)

### Connect

To connect sources and sinks into streams