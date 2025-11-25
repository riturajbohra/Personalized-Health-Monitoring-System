# Personalized Health Monitoring System

## Overview
The Personalized Health Monitoring System integrates wearable devices with AI-driven analytics to provide real-time, individualized health insights. It collects metrics from wearable devices (heart rate, steps, sleep), stores them in a relational database, and processes them to generate personalized recommendations and alerts.

## Repository Structure
```
personalized-health-monitoring/
├── README.md
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/com/example/phms/
│   │   │   ├── App.java
│   │   │   ├── config/DBConnectionUtil.java
│   │   │   ├── model/
│   │   │   │   ├── User.java
│   │   │   │   ├── Patient.java
│   │   │   │   ├── Provider.java
│   │   │   │   ├── Device.java
│   │   │   │   ├── Reading.java
│   │   │   │   └── Recommendation.java
│   │   │   ├── dao/
│   │   │   │   ├── UserDao.java
│   │   │   │   ├── PatientDao.java
│   │   │   │   └── impl/ (JDBC implementations)
│   │   │   └── service/
│   │   │       └── RecommendationService.java
│   └── test/
├── sql/
│   └── schema.sql
├── docs/
│   ├── er_diagram.mmd
│   ├── architecture.mmd
│   └── uml/
│       ├── usecase.mmd
│       ├── class.mmd
│       └── sequence.mmd
└── presentation/
    └── Enhanced_Presentation.pptx
```

## Setup & Requirements
- Java 11+ (JDK)
- Maven 3.6+
- MySQL / PostgreSQL (or any RDBMS)
- JDBC driver for your DB in `pom.xml`

## Database Setup
Run the SQL file at `sql/schema.sql` to create required tables.
Update DB connection in `src/main/java/com/example/phms/config/DBConnectionUtil.java` with your DB URL, username, and password.

## Build & Run
```bash
mvn clean package
java -jar target/personalized-health-monitoring-1.0.jar
```

## How to Test
1. Ensure DB is running and schema is created.
2. Update `application.properties` or `DBConnectionUtil` with DB credentials.
3. Use provided sample data SQL or DataLoader to insert sample users/devices/readings.
4. Run the application and use REST endpoints (to be added) or the CLI to simulate device readings.

## Contribution & Coding Standards
- Follow Java naming conventions.
- Write modular, commented code with unit tests for services and DAOs.
- Add README sections for any new modules/features.

## Contact
Project prepared for submission and review. For queries, open an issue in the repository.
