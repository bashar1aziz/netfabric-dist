# NetFabric — Deployment Guide

## Prerequisites
- Docker + Docker Compose installed
- A valid `license.json` file (provided by NetFabric)

## Setup

**1. Clone this repo**
```bash
git clone https://github.com/basharaziz/netfabric-dist.git
cd netfabric-dist
```

**2. Configure environment**
```bash
cp .env.example .env
```
Edit `.env` and fill in:
- `SECRET_KEY` — run `openssl rand -hex 32`
- `FERNET_KEY` — run `python3 -c "from cryptography.fernet import Fernet; print(Fernet.generate_key().decode())"`
- `POSTGRES_PASSWORD` — choose a strong password (update in both `POSTGRES_PASSWORD` and `DATABASE_URL`)
- `ANTHROPIC_API_KEY` — your Anthropic key (optional, for AI analysis features)

**3. Add your license file**

Place the `license.json` file you received from NetFabric in this directory:
```
netfabric-dist/
├── docker-compose.yml
├── .env
└── license.json        ← here
```

**4. Start**
```bash
docker compose up -d
```

App is available at http://localhost:8000

## Upgrading

Pull the latest image and restart:
```bash
docker compose pull
docker compose up -d
```

## License tiers

| Tier      | Max devices |
|-----------|-------------|
| 1         | 1           |
| 10        | 10          |
| 100       | 100         |
| 1000      | 1000        |
| unlimited | No cap      |

To upgrade your license tier, contact support.
