# NetFabric

Network device management platform.

## Requirements

- Docker + Docker Compose
- `license.json` provided by NetFabric support

## Setup

```bash
git clone https://github.com/netlayer1/netfabric-dist
cd netfabric-dist
mkdir -p license
cp license.json license/license.json
cp .env.example .env   # edit with your DB credentials
docker compose up -d
```

Open **http://localhost:8000** and register your account.

## Upgrade

```bash
docker compose pull && docker compose down && docker compose up -d
```
