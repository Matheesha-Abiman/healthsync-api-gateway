# 🌉 HealthSync API Gateway

Reactive API Gateway built with Spring Cloud Gateway. It provides the single ingress point for client requests and routes traffic to HealthSync backend microservices.

## Student Information

| Field | Details |
|---|---|
| Student Name | Matheesha Abiman |
| Student Number | 241722050 |
| Slack Handle | [YOUR SLACK HANDLE - OPTIONAL] |
| GCP Project ID | `[YOUR GCP PROJECT ID]` |

> Replace the Student Number and GCP Project ID placeholders with the exact values used for the submission.

## Project Description

The API Gateway centralizes external API access and forwards incoming requests to the appropriate backend service using service discovery and load-balanced routes.

## Service Information

| Property | Value |
|---|---|
| Framework | Spring Cloud Gateway |
| Port | `7000` |
| Gateway Type | Reactive |
| Discovery | Eureka |

## Routes

| Gateway Route | Destination |
|---|---|
| `/api/v1/patients/**` | `lb://PATIENT-SERVICE` |
| `/api/v1/doctors/**` | `lb://DOCTOR-SERVICE` |
| `/api/v1/appointments/**` | `lb://APPOINTMENT-SERVICE` |

## Request Flow

```text
Client / Web App
       |
       v
API Gateway :7000
       |
       +--> PATIENT-SERVICE :8000
       +--> DOCTOR-SERVICE :8001
       +--> APPOINTMENT-SERVICE :8002
```

## Technology Stack

- Java 
- Spring Boot 3
- Spring Cloud
- Maven
- REST APIs
- Git and GitHub
- Google Cloud Platform (GCP)

## Getting Started

### Prerequisites

- JDK 21 or 25
- Maven
- Git
- MySQL and/or MongoDB as required by the service
- Node.js and npm for the web application
- GCP access for cloud deployment

### Clone

```bash
git clone <REPOSITORY_URL>
cd <REPOSITORY_FOLDER>
```

### Run

```bash
mvn clean install
mvn spring-boot:run
```

##  Parent Repository

Part of [medicare-healthsync-platform](https://github.com/Matheesha-Abiman/medicare-healthsync-platform).
