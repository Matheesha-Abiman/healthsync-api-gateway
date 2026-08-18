# 🌉 HealthSync API Gateway

Reactive API Gateway service built with **Spring Cloud Gateway**. Serves as the single ingress entry point (`http://localhost:7000`) routing external requests to backend microservices.

---

## ⚙️ Key Configuration & Routing

- **Port**: `7000`
- **Routes**:
  - `/api/v1/patients/**` ➔ `lb://PATIENT-SERVICE` (Port 8000)
  - `/api/v1/doctors/**` ➔ `lb://DOCTOR-SERVICE` (Port 8001)
  - `/api/v1/appointments/**` ➔ `lb://APPOINTMENT-SERVICE` (Port 8002)

---

## 🌐 Parent Repository

Part of [medicare-healthsync-platform](https://github.com/Matheesha-Abiman/medicare-healthsync-platform).
