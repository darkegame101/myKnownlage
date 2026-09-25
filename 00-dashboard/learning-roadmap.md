# Learning Roadmap

Sequential, prerequisite-driven learning path tailored to current knowledge levels, targeting Backend Development & DevOps competence.

---

## Phase 1: Java Ecosystem & Build Tools Foundation

### Step 1.1: Maven & Dependency Management
- **Topic**: Apache Maven Build Tool
- **Current Level**: 0/5
- **Target Level**: 4/5
- **Why Needed**: Prerequisite for managing Java libraries, build lifecycles, and Spring Boot projects.
- **Prerequisites**: Java Core (Level 3/5), JDK installation.
- **What to Learn**: `pom.xml` structure, dependencies, repositories, plugins, build lifecycle (`clean`, `compile`, `test`, `package`, `install`), multi-module projects.
- **Practical Proof Task**: Create a Maven multi-module Java project, add external dependencies (Jackson JSON parser, JUnit 5), compile and package into an executable JAR.
- **Expected Evidence**: Git repo containing `pom.xml`, passing `mvn clean package` command output.

### Step 1.2: Java 8+ Modern Features & Streams API
- **Topic**: Java 8 Streams API, Lambdas & Functional Interfaces
- **Current Level**: 1/5
- **Target Level**: 4/5
- **Why Needed**: Prerequisite for modern Spring Boot backend coding.
- **Prerequisites**: Java Core & Collections (Level 3/5).
- **What to Learn**: Functional Interfaces (`Supplier`, `Consumer`, `Function`, `Predicate`), Lambda syntax, Streams API (`map`, `filter`, `reduce`, `collect`, `flatMap`), `Optional` class.
- **Practical Proof Task**: Refactor standard collection loop exercises (Student Management) to use Java Streams API pipeline.
- **Expected Evidence**: Unit-tested Java class performing complex collection filtering/mapping using Streams.

### Step 1.3: Java Unit Testing (JUnit 5 & Mockito)
- **Topic**: Automated Testing in Java
- **Current Level**: 0/5
- **Target Level**: 4/5
- **Why Needed**: Essential for verifying code correctness and building CI/CD test automation.
- **Prerequisites**: Java Core, Maven.
- **What to Learn**: JUnit 5 annotations (`@Test`, `@BeforeEach`, `@ParameterizedTest`), Assertions (`assertEquals`, `assertThrows`), Mockito mocking framework (`@Mock`, `@InjectMocks`, `when().thenReturn()`).
- **Practical Proof Task**: Write unit test suite achieving >80% code coverage for Java domain service classes and mock DAO dependencies.
- **Expected Evidence**: JUnit XML test reports generated via Maven test runner.

---

## Phase 2: Linux Networking & Containerization Fundamentals

### Step 2.1: Advanced Linux Networking & Network Namespaces
- **Topic**: Linux Network Namespaces, Bridges & NAT
- **Current Level**: 1/5
- **Target Level**: 4/5
- **Why Needed**: Direct prerequisite for understanding Docker bridge networks and port forwarding.
- **Prerequisites**: Linux SysAdmin (Level 3/5), Networking Sockets (Level 3/5).
- **What to Learn**: `ip netns` (creating isolated network namespaces), virtual ethernet pairs (`veth`), Linux Bridge (`ip link add br0 type bridge`), IP Forwarding (`sysctl net.ipv4.ip_forward=1`), `iptables` NAT masquerading and port forwarding.
- **Practical Proof Task**: Manually create 2 Linux network namespaces connected via a Linux bridge, assign static IP addresses, enable `iptables` NAT, and ping external internet from inside the isolated namespace.
- **Expected Evidence**: Executable Bash script reproducing custom Linux network namespace topology.

### Step 2.2: Docker Containerization Fundamentals & Networking
- **Topic**: Docker Containers, Dockerfile & Docker Networks
- **Current Level**: 0/5
- **Target Level**: 4/5
- **Why Needed**: Core DevOps and Backend deployment technology.
- **Prerequisites**: Linux CLI (Level 3/5), Linux Network Namespaces (Step 2.1).
- **What to Learn**: Docker Engine architecture, Docker images vs containers, Docker CLI (`docker run`, `ps`, `exec`, `logs`), writing efficient multi-stage `Dockerfile`s, Docker volumes, Docker Networks (`bridge`, `host`, custom bridge), Docker Compose (`docker-compose.yml`).
- **Practical Proof Task**: Containerize a Java backend app and SQL Server DB using `docker-compose.yml`. Inspect bridge network interfaces (`docker network inspect`).
- **Expected Evidence**: Functional `Dockerfile` and `docker-compose.yml` with single-command deployment.

---

## Phase 3: Modern Backend Development & ORM

### Step 3.1: Spring Boot & Spring Data JPA
- **Topic**: Spring Boot Framework, REST API & JPA ORM
- **Current Level**: 0/5
- **Target Level**: 4/5
- **Why Needed**: Industry standard framework for Java Web/Backend engineering.
- **Prerequisites**: Java Core (Level 3/5), Maven (Step 1.1), Streams (Step 1.2), SQL Server & JDBC (Level 3/5).
- **What to Learn**: Dependency Injection (IoC Container), Spring Web MVC (`@RestController`, `@GetMapping`, `@PostMapping`), Spring Data JPA (`@Entity`, `@Table`, `JpaRepository`), HikariCP connection pool configuration, Exception Handler (`@RestControllerAdvice`).
- **Practical Proof Task**: Build a RESTful Web API for E-commerce product catalog with full CRUD operations, pagination, and database persistence.
- **Expected Evidence**: Open-source GitHub repository with functional REST API endpoints and integration tests.

---

## Phase 4: CI/CD Automation & Cloud Deployment

### Step 4.1: GitHub Actions CI/CD Pipeline
- **Topic**: GitHub Actions Automated Workflows
- **Current Level**: 0/5
- **Target Level**: 4/5
- **Why Needed**: Automates building, testing, and containerizing software on code push.
- **Prerequisites**: Git & GitHub (Level 4/5), Maven (Step 1.1), JUnit (Step 1.3), Docker (Step 2.2).
- **What to Learn**: GitHub Actions syntax (`.github/workflows/ci.yml`), triggers (`on: push`, `pull_request`), jobs, steps, environment secrets, Docker Hub image publish action.
- **Practical Proof Task**: Build a GitHub Actions workflow that automatically compiles Java code, runs JUnit tests, builds a Docker image, and pushes it to Docker Hub on every commit to main branch.
- **Expected Evidence**: Green checkmark on GitHub commit history and published Docker image tag.
