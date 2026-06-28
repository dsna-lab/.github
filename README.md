# Welcome to DSNA Lab 👋

An interactive, multi-service Data Structures and Algorithms (DSA) playground and visualizer built to make computer science concepts intuitive and engaging.

---

## 🚀 The Architecture Overview

The platform is explicitly decoupled into micro-services to handle independent scalability, clear division of responsibilities, and future streaming architectures.

* **[dsna-web-app](https://github.com/dsna-lab/dsna-web-app)**: High-performance frontend leveraging Angular (v19) to render real-time visual states, control step-by-step playback speeds, and provide responsive dashboards.
* **[dsna-visualization-service](https://github.com/dsna-lab/dsna-visualization-service)**: The orchestration gateway and middleware running on Spring Boot. It dynamically computes algorithmic mutations and serves them as discrete frame states to the UI.
* **[dsna-core-service](https://github.com/dsna-lab/dsna-core-service)**: The secure backend infrastructure handling centralized domain operations, User Authentication (JWT), user preference configurations, and persistent PostgreSQL storage mappings.
* **[dsna-infra](https://github.com/dsna-lab/dsna-infra)**: Central container orchestration home holding platform `docker-compose` setups, network topologies, and environmental declarations.

---

## 🛠️ Technology Stack

| Layer | Technologies |
| :--- | :--- |
| **Frontend** | Angular 19, TypeScript, RxJS, CSS Variables |
| **Gateway & Computation** | Java 21, Spring Boot, WebSockets / REST |
| **Persistence & Business** | Java 21, Spring Boot, Spring Data JPA, PostgreSQL |
| **Infrastructure** | Docker, Docker Compose, Nginx Proxying |

---

## 🚦 Local Quickstart

Want to spin up the entire multi-service ecosystem locally? Ensure you have **Docker Desktop** installed, then execute:

```bash
# 1. Clone the environment infrastructure repository
git clone [https://github.com/dsna-lab/dsna-infra.git](https://github.com/dsna-lab/dsna-infra.git)
cd dsna-infra

# 2. Compile all microservices and launch unified containers
docker compose up -d --build

```

Frontend UI: Open your browser and navigate to http://localhost:3000 to interact with the visualizer.

Gateway API: Monitor backend metrics and routing health at http://localhost:8081.

Core API: Access persistent configuration data endpoints at http://localhost:8080.

📬 Contact & Contributions
Feel free to open issues or pull requests across our repositories to add new algorithmic visualizations or submit structural improvements!
