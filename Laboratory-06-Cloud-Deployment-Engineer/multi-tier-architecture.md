# Multi-Tier Architecture — Nextcloud Deployment

## Overview
This project implements a **2-tier architecture** deployed using Docker and Docker Compose. The system consists of separate containers for the web application and the database, running together as a coordinated stack.

## Architecture Diagram
[Client / Browser]
↓ (HTTP :8000)
┌──────────────┐
│ App Tier │
│ nextcloud │ ← Web Interface & Application Logic
│ (Port 8000) │
└──────┬───────┘
│ Internal Docker Network
↓
┌──────────────┐
│ Data Tier │
│ mariadb:10.6│ ← Persistent Storage
│ (Database) │
└──────────────┘

## Components

### 1. Application Tier — `app` Service
- **Image**: `nextcloud`
- **Function**: Handles user interface, file management, authentication, and all web requests
- **Port**: `8000` (host) → `80` (container)
- **Volumes**: Stores application data persistently
- **Communicates with**: Database using service name `db` as hostname

### 2. Data Tier — `db` Service
- **Image**: `mariadb:10.6`
- **Function**: Stores user accounts, file metadata, permissions, and system configuration
- **Not exposed externally** — accessible only within the internal Docker network
- **Volumes**: `/var/lib/mysql` — ensures data survives container restarts

## Why Separate Containers?

| Benefit | Explanation |
|---|---|
| **Isolation** | Database credentials and data are not exposed through the web container |
| **Scalability** | Can restart, update, or replace one component without affecting the other |
| **Maintainability** | Clearer structure; easier to debug and modify |
| **Reliability** | If the web app fails, the database continues running; data integrity is preserved |
| **Reusability** | Database can be reused by other services independently |

## How They Connect
- Docker provides **internal DNS resolution** → the `app` container finds the database at hostname `MYSQL_HOST=db`
- Credentials are passed securely through **environment variables** — not hardcoded in the image
- Persistent **named volumes** preserve data even when containers are removed

## File Structure

## Commands Reference
| Command | Action |
|---|---|
| `docker compose up -d` | Start all services in background |
| `docker compose ps` | Check running containers |
| `docker compose logs` | View combined logs |
| `docker compose down` | Stop and remove containers & network |

## Conclusion
This deployment demonstrates how multi-tier architecture principles apply to containerized workloads. By separating concerns into dedicated services — presentation and data — we achieve a system that is secure, maintainable, and scalable.
