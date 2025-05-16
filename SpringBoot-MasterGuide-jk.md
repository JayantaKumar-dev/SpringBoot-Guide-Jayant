# 🌱 Spring Boot Mastery Guide (2025 Edition)

## 📘 Table of Contents
1. Introduction to Spring Boot

2. Getting Started

3. Spring Boot Core Concepts

4. Dependency Injection and Configuration

5. Spring Boot REST APIs

6. Data Access with Spring Data JPA

7. Spring Boot Security (Latest 2025 Practices)

8. Exception Handling

9. Testing in Spring Boot

10. Advanced Topics

11. Real-World Project Ideas

12. Resources and Further Learning


# ✅ Learning Goals
### By the end of this guide, you will:

- Understand Spring Boot from scratch

- Build real-world RESTful APIs

- Secure your application with JWT and Spring Security (2025 updates)

- Handle exceptions like a pro

- Master testing (unit + integration)

- Deploy applications to cloud environments

- Follow best practices for maintainability and performance


# 1. Introduction to Spring Boot

# 🧠 What is Spring Boot?
Spring Boot is a Java framework that helps developers create web applications and microservices faster and more easily. It's built on top of the Spring Framework, an open-source framework for creating applications that run on the Java virtual machine (JVM).  

## 🎯 Why Use Spring Boot?

- Auto Configuration: Automatically configures beans based on dependencies.

- Embedded Server: Run apps without needing external Tomcat/Jetty.

- Starter Dependencies: Convenient dependency management.

- Production Ready: Built-in Actuator, metrics, and monitoring.

## 🧱 Spring Boot vs Spring Framework
| Feature           | Spring Framework       | Spring Boot          |
|-------------------|------------------------|----------------------|
| Configuration     | Manual, verbose        | Auto-configured      |
| Server setup      | External container     | Embedded server      |
| Learning curve    | Steep                  | Beginner-friendly    |
| Application size  | Lightweight            | Lightweight          |


# 2. Getting Started
### 📦 Prerequisites
- Java 17 or 21 (Recommended in 2025)

- Maven or Gradle

- IDE (IntelliJ IDEA, VS Code, STS, Eclipse)

- Postman/Swagger (for API testing & documentation)

- Database (e.g: MySQL, MongoDB)

#🛠️ Creating Your First Spring Boot Project

✅ Option 1: Using Spring Initializr (Recommended)

- Visit: https://start.spring.io/

- Project: Maven

- Language: Java

- Spring Boot Version: 3.2.x (Latest stable)

- Dependencies:

  - Spring Web
  
  - Spring Boot DevTools
  
  - Lombok

Click Generate, extract the .zip, and open it in your IDE.

# 📁 Folder Structure
```bash
src
└── main
    ├── java
    │   └── com.example.demo
    │       ├── controller
    │       ├── service
    │       ├── model
    │       └── DemoApplication.java
    └── resources
        ├── application.properties
        └── static / templates
```

# 👨‍💻 Writing Your First API

### Step 1: Main Application Class
Note: It is bydefault present in default package no need to change
```java
@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

### Step 2: HelloController

```java
@RestController
@RequestMapping("/api")
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Spring Boot 2025!";
    }
}
```
### Step 3: application.properties

```properties
server.port=8080
spring.application.name=demo-app
```
### Run Application
```bash
# In terminal or IDE
mvn spring-boot:run
```
Visit: http://localhost:8080/api/hello (in postman or browser)

#### Expected Output:
```text
Hello, Spring Boot 2025!
```
