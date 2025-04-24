# 🐳 NeuroDock: Complex Docker-Based Neural Simulation Environment

NeuroDock is a high-performance, containerized environment designed for distributed neural simulation using Docker. This system leverages multiple services—each isolated in containers—to simulate and analyze artificial brain activity in real-time with GPU acceleration, message queues, and efficient data pipelines.

---

## 🏗️ System Architecture (Docker-Only)

This project runs the following services using Docker:

- `neuro-ingest`: Streams real-time neural data (mocked for dev).
- `neuro-cleaner`: Processes and normalizes raw input data.
- `neuro-core`: Runs the GPU-accelerated simulation engine (CUDA).
- `neuro-api`: Exposes a REST API for external access (FastAPI).
- `redis`: In-memory cache for preprocessed data.
- `postgres`: Stores simulation results and metadata.
- `kafka`: Manages inter-container communication.

Each service is defined in a single `docker-compose.yml` file.

---

## 🐋 Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)
- NVIDIA GPU with [nvidia-container-toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html) installed (optional but recommended)

---

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/youruser/neurodock.git
   cd neurodock


