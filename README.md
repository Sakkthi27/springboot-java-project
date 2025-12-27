

## Spring Boot Java Project – Maven Build & Run Guide

This guide explains how to set up Java, Maven, clone the project, build it using Maven lifecycle phases, and run the Spring Boot application.

---

## Prerequisites

* Ubuntu / Debian-based Linux
* Internet access
* sudo privileges

---

## Step 1: Update System Packages

```bash
sudo apt-get update -y
```

---

## Step 2: Install Java (OpenJDK 11)

```bash
sudo apt install openjdk-11-jre -y
java --version
```

---

## Step 3: Install Maven

```bash
sudo apt install maven -y
mvn -version
```

---

## Step 4: Clone the Spring Boot Project

```bash
git clone https://github.com/Sakkthi27/springboot-java-project.git
cd springboot-java-project/
ls
```

---

## Step 5: Maven Lifecycle Commands

### 1. Validate Project Structure

```bash
mvn validate
```

---

### 2. Compile the Source Code

```bash
mvn compile
```

---

### 3. Run Unit Tests

```bash
mvn test
```

---

### 4. Package the Application (JAR)

```bash
mvn package
```

Check the generated artifacts:

```bash
ls
cd target
ls
cd ..
```

---

### 5. Install the Package to Local Repository

```bash
mvn install
```

---

### 6. Clean Old Build Files

```bash
mvn clean
```

---

### 7. Clean and Package (Recommended for CI/CD)

```bash
mvn clean package
```

Verify the JAR file:

```bash
cd target
ls
cd ..
```

---

## Step 6: Run the Spring Boot Application

```bash
java -jar target/spring-boot-web.jar
```

✅ The application should now start successfully.

---

## Maven Lifecycle Summary

| Phase    | Purpose                     |
| -------- | --------------------------- |
| validate | Validate project structure  |
| compile  | Compile source code         |
| test     | Run unit tests              |
| package  | Create JAR/WAR              |
| install  | Install to local Maven repo |
| clean    | Remove old build files      |

---

## Notes for DevOps / CI-CD

* Use `mvn clean package` in Jenkins/GitHub Actions
* Artifact location: `target/spring-boot-web.jar`
* Java version: **OpenJDK 11**
* Build tool: **Apache Maven**


