# Quotes API Service 💬

A lightweight, production-ready REST API service built with **Spring Boot** that provides random inspirational quotes. Perfect for learning Spring Boot, Docker containerization, and microservices architecture.

## 📋 Overview

**Quotes API** is a simple yet powerful microservice that delivers random inspirational quotes through a clean REST API. This project demonstrates:
- Spring Boot best practices
- Docker containerization
- RESTful API design
- Microservices architecture patterns

## ✨ Features

- 🎲 **Random Quote Generation** - Get a fresh inspirational quote with each request
- 🚀 **Lightweight & Fast** - Built with Spring Boot for optimal performance
- 🐳 **Docker Ready** - Complete Docker configuration included
- 📦 **Production Ready** - Follows Spring Boot best practices
- 🔄 **Stateless Design** - Perfect for microservices architecture

## 🛠️ Technology Stack

- **Java** - Core programming language
- **Spring Boot** - Application framework
- **Maven** - Build and dependency management
- **Docker** - Containerization

## 🚀 Getting Started

### Prerequisites

- Java 8 or higher
- Maven 3.x
- Docker (optional, for containerized deployment)

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/bhanuchaddha/quotes.git
cd quotes
```

2. **Build the project:**
```bash
./mvnw clean install
```

3. **Run the application:**
```bash
./mvnw spring-boot:run
```

The service will start on `http://localhost:8080`

### Docker Deployment

1. **Build Docker image:**
```bash
docker build -t quotes-service .
```

2. **Run container:**
```bash
docker run -p 8080:8080 quotes-service
```

## 📡 API Endpoints

### Get Random Quote

**Endpoint:** `GET /random-quote`

**Response:**
```json
{
    "result": "An obstacle may be either a stepping stone or a stumbling block.",
    "setOrExpired": true
}
```

**Example:**
```bash
curl http://localhost:8080/random-quote
```

## 🏗️ Project Structure

```
quotes/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/lct/tutorial/quotes/
│   │   │       └── QuotesApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/
│           └── com/lct/tutorial/quotes/
│               └── QuotesApplicationTests.java
├── Dockerfile
├── pom.xml
└── README.md
```

## 🐳 Docker Configuration

The project includes a complete Dockerfile for easy containerization:

```dockerfile
FROM openjdk:8-jre-alpine
COPY target/quotes-*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

## 📚 Tutorial

This repository has been used to demonstrate Docker containerization of Spring Boot applications. Check out the detailed tutorial:

**[Containerize Spring Boot Application with Docker](https://medium.com/@bhanuchaddha/containerise-spring-boot-application-with-docker-6d395c529f44)**

## 🧪 Testing

Run the test suite:

```bash
./mvnw test
```

## 🔧 Configuration

Application properties can be configured in `src/main/resources/application.properties`:

```properties
server.port=8080
# Add your custom configurations here
```

## 📦 Building for Production

1. **Create JAR file:**
```bash
./mvnw clean package
```

2. **Run JAR:**
```bash
java -jar target/quotes-*.jar
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🌟 Use Cases

- **Learning Spring Boot** - Perfect starter project
- **API Gateway Integration** - Use as a microservice
- **Mobile App Backend** - Provide quotes to mobile apps
- **Dashboard Widgets** - Display inspirational quotes
- **CI/CD Practice** - Learn Docker and deployment

## 🔗 Related Resources

- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Docker Documentation](https://docs.docker.com/)
- [REST API Best Practices](https://restfulapi.net/)

---

**Built with Spring Boot ❤️**
