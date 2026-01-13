# pangolin-homelab

Infrastructure as code for deploying a **Pangolin Home Lab** environment using Docker Compose.

This repository contains example configuration for running Pangolin (zero-trust VPN + reverse proxy) within a homelab or VPS environment.

Pangolin is an **open-source identity-based remote access platform** built on WireGuard that enables secure access to private and public resources with a zero-trust model. It combines reverse proxy and VPN capabilities in one platform to expose apps and connect to services without exposing your network directly to the internet. :contentReference[oaicite:0]{index=0}

---

## 🚀 Components

This repo includes:

| File | Purpose |
|------|---------|
| `compose.yaml` | Docker Compose definition for launching Pangolin and supporting services. |
| `config.yaml` | Base configuration for the Pangolin server. |
| `dynamic_config.yaml` | Overridable runtime configuration settings. |
| `traefik_config.yaml` | Traefik reverse proxy configuration for web UI routing. |
| `traefik-dashboard.yaml` | Optional Traefik dashboard/service routing config. |

---

## 🧱 Architecture

This setup is intended to run locally in a homelab or on a small VPS and provides:

- **Secure remote access** to homelab services via Pangolin
- **Reverse proxy routing** using Traefik
- **Containerized deployment** using Docker Compose

---

## 📦 Requirements

- Docker 20.10+
- Docker Compose
- A domain with DNS records pointing to your host (optional but recommended)
- Firewall allowing access to necessary ports (e.g., WireGuard / HTTP/HTTPS)

---

## 🛠 Quick Setup

1. **Clone the repo**
   ```sh
   git clone https://github.com/dinjojo/pangolin-homelab.git
   cd pangolin-homelab
