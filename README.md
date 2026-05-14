# Spring Boot Java Archetype

Maven archetype for generating a Spring Boot REST API project.

## Requirements

- Java 8+
- Maven 3+

---

# Install Archetype Locally

Clone the repository and install the archetype into your local Maven repository:

```bash
mvn clean install
```

---

# Generate a Project

Run the following command:

```bash
mvn archetype:generate \
  -DarchetypeGroupId=com.chedi \
  -DarchetypeArtifactId=spring-boot-java-archetype \
  -DarchetypeVersion=0.0.1-SNAPSHOT \
  -DgroupId=com.example.demo \
  -DartifactId=my-spring-api \
  -Dversion=1.0.0 \
  -DinteractiveMode=false
```

---

# Generated Project Structure

```text
my-spring-api/
├── pom.xml
├── mvnw
├── mvnw.cmd
├── Dockerfile
├── README.md
└── src
    ├── main
    │   ├── java
    │   └── resources
    └── test
```

---

# Run the Application

```bash
cd my-spring-api
mvn spring-boot:run
```

Application will start on:

```text
http://localhost:8080
```

---

# Swagger UI

```text
http://localhost:8080/swagger-ui.html
```

---

# Technologies

- Spring Boot
- Spring Web
- Spring Data JPA
- PostgreSQL
- H2 Database
- Lombok
- Swagger

---

# Author

Chedi