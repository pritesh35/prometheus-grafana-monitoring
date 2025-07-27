# Basic Monitoring Stack with Prometheus & Grafana

This project sets up a basic application monitoring stack using **Prometheus** for metrics collection and **Grafana** for visualization. The entire stack is orchestrated with **Docker Compose**.

![Grafana Dashboard Screenshot](![Dashboard Screenshot](https://github.com/user-attachments/assets/eb1e0599-9cff-40dd-ae56-5277738ac33))
*(Pro tip: Take a screenshot of your final dashboard, upload it to the GitHub issue tracker, and paste the URL here.)*

## Prerequisites

-   Docker
-   Docker Compose

## How to Run

1.  Clone the repository:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git)
    ```
2.  Navigate into the project directory:
    ```bash
    cd YOUR_REPOSITORY
    ```
3.  Start the services:
    ```bash
    docker-compose up -d
    ```
4.  Access the services:
    -   **Grafana**: `http://localhost:3000` (Login: admin/admin)
    -   **Prometheus**: `http://localhost:9090`

## Configuration

-   **`docker-compose.yml`**: Defines the three services (Prometheus, Grafana, Node Exporter) and uses a named volume `grafana-data` to persist Grafana dashboards.
-   **`prometheus.yml`**: Configures Prometheus to scrape metrics from the Node Exporter service every 15 seconds.
