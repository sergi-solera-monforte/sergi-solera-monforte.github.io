---
layout: page
title: TutorChat Modernization
description: Refactoring and Dockerization of a legacy Intelligent Tutoring System.
img: assets/img/tutorchat_k8s.png
importance: 1
category: engineering
related_publications: false
---

**The Challenge:**
The original *TutorChat* system was a classic legacy monolith. Built on obsolete technologies (JSP, Servlets), it suffered from tight coupling, "dependency hell" (manual JAR management), and a fragile deployment process that made scalability impossible.

**The Engineering Solution:**
My Final Degree Project focused on a complete architectural overhaul to transition this system into a cloud-native environment. The project was executed in three phases:

1.  **Backend Refactoring:** Migrating from raw Servlets to **Spring Boot**, implementing a clean **Layered Architecture** (Controller, Service, Repository) to decouple logic from data access.
2.  **Frontend Decoupling:** Replacing server-side rendering (JSP) with a modern **React** Single Page Application (SPA).
3.  **DevOps & Containerization:** Dockerizing services and orchestrating the deployment using **Kubernetes**.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tutorchat.png" title="TutorChat Interface" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The modernized User Interface built with React, providing a real-time, responsive chat experience for collaborative learning.
</div>

### Infrastructure as Code (IaC)

A critical component of this project was ensuring **reproducibility**. I replaced manual server configuration with Docker containers. The application was split into two primary containers (Frontend and Backend) interacting with a MySQL database.

To achieve high availability and scalability, I deployed the stack on a **Kubernetes** cluster (using MicroK8s for local simulation). This involved writing `Deployment` and `Service` manifests to handle pod orchestration and networking.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tutorchat_k8s.png" title="Kubernetes Cluster" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The final deployment architecture running on Kubernetes, orchestrating the React Frontend, Spring Boot API, and MySQL Database.
</div>

### Key Technical Achievements
* **Reduced Technical Debt:** Eliminated obsolete dependencies and standardized build management using **Maven**.
* **Improved Maintainability:** Implemented the **DAO Pattern** (Data Access Object) via Hibernate/JPA, removing raw SQL queries from business logic.
* **Scalability:** The move to Kubernetes allows the API to scale horizontally based on student load, a critical feature for educational environments.