# Cloud / Docker Deployment Project

A containerized application/deployment experiment using **Java/Maven, Docker, Docker Compose, and Docker Swarm**.



## Build and deployment flow

```text
Java application
      ↓
Maven build
      ↓
Docker image build
      ↓
Docker Compose definition
      ↓
Docker Swarm stack deployment
```

## Build

Build the Java artifacts:

```bash
mvn clean install -DskipTests
```

Build the container images:

```bash
docker-compose build
```

Deploy the stack to Docker Swarm:

```bash
docker stack deploy -c docker-compose.yml <your_stack_name>
```

## What this repository demonstrates

- packaging an application with Docker;
- multi-service orchestration with Compose;
- deployment through Docker Swarm stacks;
- integrating a Java/Maven build with container infrastructure.


