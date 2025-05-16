# Event_driven_microservice

Event-driven microservice for processing user activity logs using Node.js, Kafka, MongoDB, Docker, and Kubernetes.

## Architecture

- **Domain-Driven Design**: Implements DDD with clear separation of domain entities, aggregates, and services.
- **Event-Driven**: Uses Kafka for real-time activity processing.
- **Persistence**: MongoDB with proper indexing for efficient querying.
- **API**: REST API with pagination and filtering.
- **Deployment**: Dockerized and orchestrated with Kubernetes.

### Architecture Choices
- **DDD**: Ensures clear domain boundaries and maintainable code structure.
- **Kafka**: Provides scalable, fault-tolerant event processing.
- **MongoDB**: Flexible schema for activity logs with efficient indexing.
- **Node.js**: Lightweight and performant for I/O-heavy operations.
- **Kubernetes**: Enables scalability and resilience.

## Setup Instructions

1. **Prerequisites**
   - Docker
   - Kubernetes (Minikube or cloud provider)
   - Kafka cluster
   - MongoDB
   - Node.js

2. **Clone Repository**
   ```bash
   git clone <repository-url>
   cd user-activity-service

3. **Environment Setup**
   ```bash
   cp .env.example .env
   
4. **Build and Run Locally**
     ```bash
   npm install
   docker build -t user-activity-service .
   docker run -p 3000:3000 --env-file .env user-activity-service
     
5. **Deploy to Kubernetes**
    ```bash
   kubectl apply -f k8s/deployment.yaml
   kubectl apply -f k8s/service.yaml


