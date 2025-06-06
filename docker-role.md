# 🐳 Ansible Role: Docker Engine Installer

This Ansible role handles the installation, configuration, and optional hardening of the Docker Engine on Linux-based edge nodes.

## 📦 Key Features

- 📥 Installs Docker CE from official repos
- 🎯 Supports Debian, Ubuntu, CentOS, and RHEL
- 🛡️ Optionally configures firewalld for Docker Swarm
- 👥 Adds users to `docker` group
- 🔁 Reloads systemd & restarts Docker gracefully

## 🔧 Role Variables

```yaml
docker_version: "20.10.24"
docker_users:
  - codexadmin
  - deployagent
enable_firewall_docker_ports: true
use_podman_fallback: false
roles/
└── docker/
    ├── tasks/
    │   ├── install.yml
    │   └── configure.yml
    ├── defaults/
    │   └── main.yml
    ├── handlers/
    │   └── restart.yml
    ├── templates/
    │   └── daemon.json.j2
