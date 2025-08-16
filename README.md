# Observability-For-DevOps

This repository provides a comprehensive observability stack tailored for DevOps engineers. It integrates key tools like Prometheus, Grafana, cAdvisor, and Node Exporter to monitor, visualize, and manage your infrastructure and applications. Additionally, it includes a custom Notes App to demonstrate the observability stack in action.

<img width="1914" height="952" alt="Screenshot 2025-08-16 125902" src="https://github.com/user-attachments/assets/170625ad-9b20-44c5-9d4e-049d30ad84db" />

<img width="1919" height="924" alt="Screenshot 2025-08-16 130444" src="https://github.com/user-attachments/assets/a4e6eb66-04c3-4c19-899f-b18bde6e136c" />


## Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Services](#services)
- [Volumes](#volumes)
- [Network](#network)
- [Monitoring Setup](#monitoring-setup)
- [Contributing](#contributing)
- [License](#license)

## Overview
In modern DevOps, observability is key to ensuring the health and performance of your applications and infrastructure. This repository sets up an observability stack that includes metrics collection, container monitoring, and real-time visualization.

## Tech Stack
- **Docker & Docker Compose**: Containerization and orchestration.
- **Prometheus**: Metrics collection and monitoring.
- **Grafana**: Data visualization and dashboard creation.
- **cAdvisor**: Container resource monitoring.
- **Node Exporter**: Hardware and OS metrics exporter.
- **Notes App**: A custom service to demonstrate monitoring.

## Features
- Real-time monitoring of container metrics with Prometheus.
- Visualize metrics using Grafana dashboards.
- Monitor hardware, OS metrics, and custom application performance.
- Easily extendable for additional services and metrics.
- Persistent data storage for Prometheus and Grafana.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/Observability-For-DevOps.git
    cd Observability-For-DevOps
    ```

2. **Ensure Docker and Docker Compose are installed**:
    - [Docker Installation Guide](https://docs.docker.com/get-docker/)
    - [Docker Compose Installation Guide](https://docs.docker.com/compose/install/)

3. **Download Prometheus config file**:
    ```bash
    wget https://raw.githubusercontent.com/prometheus/prometheus/main/documentation/examples/prometheus.yml
    ```
    
4. **Run the stack**:
    ```bash
    docker compose up -d
    ```

## Usage

- Access **Grafana** at `http://localhost:3000`
  - Default credentials: `admin` / `admin` (you'll be prompted to change this)
- Access **Prometheus** at `http://localhost:9090`
- Access **cAdvisor** at `http://localhost:8080`
- **Node Exporter** metrics will be available at `http://localhost:9100/metrics`
- Access **Notes App** at `http://localhost:8000`

## Services

- **Grafana**: Visualization tool for Prometheus data.
- **Prometheus**: Collects and stores metrics.
- **Node Exporter**: Exports hardware and OS-level metrics.
- **cAdvisor**: Provides container resource usage and performance metrics.
- **Notes App**: Sample application to demonstrate monitoring.

## Volumes

- `prometheus_data`: Stores Prometheus data persistently.
- `grafana_data`: Stores Grafana dashboards and data persistently.

## Network

- **monitoring**: Custom bridge network to ensure isolation and communication between services.

## Monitoring Setup

- **Grafana Dashboards**: Pre-configured to visualize data from Prometheus.
- **Prometheus Configuration**: Configured to scrape metrics from Node Exporter, cAdvisor, and Notes App.

## some sample shots
<img width="1919" height="968" alt="Screenshot 2025-08-16 132521" src="https://github.com/user-attachments/assets/9a2f575b-4000-4a6c-a858-7b0d12340df3" />

<img width="1919" height="950" alt="Screenshot 2025-08-16 130433" src="https://github.com/user-attachments/assets/40aa3dfc-748d-450b-9b44-4f96e99dbba3" />

<img width="1540" height="528" alt="Screenshot 2025-08-16 132501" src="https://github.com/user-attachments/assets/0defcff3-a756-40cf-976e-475ab867d5be" />

<img width="1913" height="959" alt="Screenshot 2025-08-16 132545" src="https://github.com/user-attachments/assets/a6570224-7619-497d-93e5-b9a29626349f" />

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for any changes or improvements.

## License

Author: Suyash Dahitule
