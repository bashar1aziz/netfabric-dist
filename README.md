# NetFabric

Network device management platform.

## Setup

```bash
git clone https://github.com/bashar1aziz/netfabric-dist
cd netfabric-dist
docker compose up -d
```

Open **http://localhost:8000** and register your account.

On first login a license banner will appear at the top — click **Upload License**, select the `license.json` file provided by NetFabric support, and click **Activate**.

## Requirements

- Docker + Docker Compose
- `license.json` provided by NetFabric support

## Upgrade

```bash
docker compose pull && docker compose up -d
```
