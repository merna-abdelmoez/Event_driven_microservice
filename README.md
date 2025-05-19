# Event_driven_microservice

Event-driven microservice for processing user activity logs using Node.js, Kafka, MongoDB, Docker, and Kubernetes.

## Architecture

- **Domain-Driven Design**: Implements DDD with clear separation of domain entities, aggregates, and services.
- **Event-Driven**: Uses Kafka for real-time activity processing.
- **Persistence**: MongoDB with proper indexing for efficient querying.
- **API**: REST API with pagination and filtering.
- **Deployment**: Dockerized and orchestrated with Kubernetes.

### Architecture Choices
- **DDD**: I split the code into domain, application, and infrastructure folders to keep things organized. The domain folder has the core logic, like the UserActivity class, so it’s not mixed with database or Kafka code.
- **Kafka**: I used Kafka to handle user activities in real time.
- **MongoDB**: Flexible for storing activity data, which might have different fields. I added indexes on userId, action, and timestamp to make the API queries faster, especially for filtering and pagination.
- **Node.js**: It’s fast for handling network stuff like API requests and Kafka messages.
- **Docker and Kubernetes for Deployment**: Docker ensures consistent environments across development and production, while Kubernetes provides scalability and resilience.

## Setup Instructions

1. **Prerequisites**
   - Docker
   - Kubernetes (Minikube or cloud provider)
   - Kafka cluster
   - MongoDB
   - Node.js

2. **Clone Repository**
   ```bash
   git clone <merna-abdelmoez/Event_driven_microservice>
   cd user-activity-service

3. **Environment Setup**
   ```bash
   cp .env.example .env
   
4. **Build and Run Locally**
     ```bash
   npm install

     
5. **Start Kafka and other services**
    ```bash
   docker-compose up -d

6.**Start the microservices**
   ```bash
   npm start

