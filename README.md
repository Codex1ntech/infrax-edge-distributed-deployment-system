# ⚙️ INFRA-X: Distributed Deployment Framework for Edge Environments

`INFRA-X` is a modular, GitOps-friendly deployment system built to automate provisioning and configuration of distributed infrastructure — from cloud to bare-metal edge nodes.

It combines container orchestration (Docker/Podman), configuration management (Ansible), and Git-based state tracking to enable scalable, secure, and repeatable deployments.

---

## ✨ Key Features

- 🔁 **GitOps Workflow** — All infra states and configurations version-controlled via Git
- 📦 **Docker & Podman Support** — Easily containerize workloads for isolated deployment
- 🌐 **Edge Node Targeting** — Built-in inventory management for remote/low-resource devices
- 🧩 **Role-based Ansible Modules** — Preconfigured roles for nginx, node exporters, ssh hardening, and more
- 🔐 **SSH Key Rotation + Secrets Management** using environment tokens
- 🛠️ **Rollback-friendly deployments** with state snapshots

---

## 📁 Project Structure

infrax/
├── playbooks/
│ ├── deploy.yml
│ └── teardown.yml
├── roles/
│ ├── nginx/
│ ├── docker/
│ └── system-hardening/
├── inventory/
│ ├── edge-nodes.ini
├── .github/
│ └── workflows/
│ └── deploy.yml
└── README.md

---

## 🚀 Use Case Scenarios

| Scenario | Description |
|---------|-------------|
| 🏭 Factory IoT deployment | Configure sensors & devices on distributed edge units |
| 🛰️ Remote update pipelines | Push updates to low-bandwidth/offline-first devices |
| 🧪 Dev-test rollouts | Simulate production conditions in isolated containers |

---

## 📦 Technologies Used

- [Ansible](https://www.ansible.com/)
- [Docker](https://www.docker.com/)
- [Podman](https://podman.io/)
- [GitHub Actions](https://github.com/features/actions)
- [Vault (optional)](https://www.vaultproject.io/) – for secrets management

---

## 📚 Documentation

> Full documentation & role guide: [docs/](./docs)

---

## 🧠 Contributing

Contributions are welcome! If you have custom Ansible roles or integrations, feel free to submit a pull request or open an issue.

---

## 📜 License

MIT License — see [`LICENSE`](./LICENSE) file.

