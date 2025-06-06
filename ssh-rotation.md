# 🔐 SSH Key Rotation Module

This module provides a secure and automated approach to rotating SSH keys across distributed edge nodes in INFRA-X deployments.

## 🚀 Overview

As edge infrastructure scales, static SSH keys pose a major security risk. This module enables:

- 🔁 Automated key rotation across all registered nodes
- ⏱️ Scheduled regeneration and deployment of new key pairs
- 🔐 Secure storage of old keys with optional rollback
- 🧩 Compatibility with Ansible inventory and roles

## 📦 Features

| Feature                      | Description                                           |
|-----------------------------|-------------------------------------------------------|
| 🔄 Key Pair Lifecycle       | Auto-generate new keys and deprecate old ones        |
| 📤 Remote Deployment        | Push updated keys using Ansible playbooks            |
| 🧪 Dry-Run Support          | Test key changes without applying them               |
| 🔒 Encrypted Backups        | Archive rotated keys using GPG or Vault              |

## 🧰 Usage

Run the playbook below to trigger key rotation across nodes listed in `inventory/edge-nodes.ini`:

```bash
ansible-playbook playbooks/rotate-ssh.yml --ask-vault-pass
