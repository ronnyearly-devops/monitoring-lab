# Windows Infrastructure Monitoring Lab

## Overview

This project demonstrates a complete infrastructure monitoring platform built using Docker, Prometheus, Grafana, and Windows Exporter.

The platform collects and visualizes real-time system metrics from a Windows host, providing visibility into system health, resource utilization, uptime, and network activity.

## Technologies Used

* Docker
* Docker Compose
* Prometheus
* Grafana
* Windows Exporter
* PromQL
* Windows 11

## Features

### Infrastructure Monitoring

* CPU Usage Monitoring
* Memory Usage Monitoring
* Disk Usage Monitoring
* Windows Uptime Monitoring
* Prometheus Uptime Monitoring
* Network Inbound Traffic
* Network Outbound Traffic
* Target Health Monitoring

### Dashboard Visualization

The Grafana dashboard provides real-time visibility into:

* CPU Utilization
* Memory Utilization
* Disk Consumption
* System Availability
* Network Activity
* Monitoring Service Health

## Architecture

Windows Host (AIAlchemy)

* Windows Exporter

Docker Containers

* Prometheus
* Grafana

Prometheus collects metrics from Windows Exporter and Grafana visualizes the collected metrics through custom dashboards.

## Example PromQL Query

```promql
100 - (avg(rate(windows_cpu_time_total{job="windows",mode="idle"}[5m])) * 100)
```

This query calculates real-time CPU utilization percentage.

## Screenshots

Screenshots of the dashboard, Prometheus targets, Docker containers, and PromQL queries are included in this repository.

## Skills Demonstrated

* Infrastructure Monitoring
* Observability
* Containerization
* Docker Compose
* Metrics Collection
* Prometheus Query Language (PromQL)
* Grafana Dashboard Development
* Windows Systems Administration

## Future Enhancements

* Alerting with Alertmanager
* Email Notifications
* Multi-Host Monitoring
* Linux Node Exporter Integration
* Dashboard Templating
* Cloud-Based Deployment

