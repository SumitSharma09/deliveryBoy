# Delivery Boy – Real-Time Location Streaming with Apache Kafka

Event-driven **Spring Boot 4** service (Java 17) that streams delivery-partner location updates through **Apache Kafka**. It is the producer side of a real-time order-tracking system.

## Features

- **REST endpoint** that publishes location events to a Kafka topic
- **Kafka producer** built with Spring for Apache Kafka (`KafkaTemplate`)
- **Topic configuration in code** (`KafkaConfig`, `AppConstants`)
- **High-volume publishing** – one request sends 100,000 simulated location updates for load testing
- Logging of produced messages for traceability

## Tech stack

Java 17 · Spring Boot 4 · Spring Web MVC · Spring for Apache Kafka · Apache Kafka · Maven

## REST API

| Method | Endpoint | Description |
|---|---|---|
| POST | `/location/update` | Publish simulated delivery-partner location updates to Kafka |

## Getting started

1. Start Kafka locally on `localhost:9092`.
2. Run:

```bash
./mvnw spring-boot:run
```

3. Call `POST /location/update` and consume the location topic with any Kafka consumer.

## Author

**Sumit Sharma** – Java Full Stack Developer (Spring Boot, Microservices, Kafka, Spring AI)
[LinkedIn](https://www.linkedin.com/in/sumit-sharma-325a24206)
