# Eureka Service Registry - ByteBites Backend Platform

Service registration and discovery server using Netflix Eureka. It acts as the lookup service registry for all microservices in the ByteBites Food Delivery Platform, enabling dynamic peer-to-peer load balancing and service communication.

## 👨‍🎓 Student Information
* **Student Name:** Anjana Heshan
* **Student ID:** 241722056
* **Module:** ITS 2130 - Enterprise Cloud Architecture (ECA)
* **GCP Project ID:** intense-slice-505613-d3

## 📝 Component Description
The **Eureka Server** is a critical component of our Spring Cloud-based microservice architecture. It provides:
* **Service Registration:** All business microservices (`order-service`, `delivery-service`, `menu-service`, `payment-service`) register their hostnames, IP addresses, and ports here upon starting up.
* **Service Discovery:** Enables the `api-gateway` and other microservices to locate and resolve instances dynamically without hardcoding URLs.
* **Health Checks:** Monitors heartbeat signals from each registered microservice instance to automatically prune unhealthy or dead instances from the routing table.
* **High Availability Ready:** Deployed across multiple VM instances distributed in multiple zones on Google Cloud Platform (GCP) for fault tolerance.

## 🛠️ Technology Stack
* **Language/Platform:** Java 17
* **Framework:** Spring Boot 3.2.5
* **Spring Cloud Module:** Spring Cloud Starter Netflix Eureka Server 2023.0.1
* **Default Port:** `8761`

## 🚀 Getting Started & Local Setup

### Prerequisites
* JDK 17 installed
* Maven installed and configured
* **Config Server must be running** (this component pulls its active configurations from the Config Server).

### Running the Eureka Server
1. Navigate to the `eureka-server` directory:
   ```bash
   cd eureka-server
   ```
2. Run the application using the Maven Wrapper:
   ```bash
   ./mvnw spring-boot:run
   ```
3. Once running, open your web browser and navigate to the Eureka Dashboard:
   ```
   http://localhost:8761
   ```
   *Here you can view all registered microservices, their current status, and instance details.*
