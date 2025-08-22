
# Grafana & Prometheus Monitoring Stack

This project provides a ready-to-use monitoring stack using Grafana and Prometheus, orchestrated with Docker Compose. It includes pre-configured dashboards and data sources for quick observability setup.

## Features

- **Prometheus** for metrics collection
- **Grafana** for visualization, with provisioning for datasources and dashboards
- Example dashboards for business insights, system health, and Flask app monitoring

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/) (v2 recommended)

## Quick Start

1. **Clone this repository:**
	```bash
	git clone <repo-url>
	cd Grafana-Prometheus-Docker
	```

2. **Start the stack:**
	```bash
	docker compose -f graf-prom-compose.yml up -d
	```

	This will start Prometheus (on port 9090) and Grafana (on port 3000).

3. **Access the services:**
	- Prometheus: [http://localhost:9090](http://localhost:9090)
	- Grafana: [http://localhost:3000](http://localhost:3000)
	  - Default login: `admin` / `admin`

4. **Dashboards & Datasources:**
	- Grafana is pre-provisioned with example dashboards and Prometheus as the default datasource.
	- You can find dashboard JSON files in `grafana/provisioning/dashboards/`.

## Stopping the stack

To stop and remove the containers, run:

```bash
docker compose -f graf-prom-compose.yml down
```

## Customization

- **Prometheus config:** Edit `prometheus.yml` to add/remove scrape targets.
- **Grafana dashboards:** Add or modify dashboards in `grafana/provisioning/dashboards/`.
- **Grafana datasources:** Edit `grafana/provisioning/datasources/datasources.yaml`.

---
For more details, see the official [Grafana documentation](https://grafana.com/docs/) and [Prometheus documentation](https://prometheus.io/docs/).
