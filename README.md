# Real Estate Listing Portal

## Solution Summary
Production-ready domain application.

This Phase-2 implementation is a domain-ready, deployable web application for **FinTech** workflows.

## Core Capabilities
- Responsive dashboard with KPI cards and recent activity table
- Domain record lifecycle with full CRUD (web + API)
- Dynamic schema fields tailored to this use case
- Status pipeline: `logged, reconciled, audited, reported`
- Docker + Gunicorn deployment assets, CI checks, and Pytest tests

## Domain Model
- Primary entity: **Real Estate Ledger Entry**
- Collection: **Real Estate Ledger Entries**
- Dynamic fields:
- Account/Wallet (`account_or_wallet` / text)
- Amount (`amount` / number)
- Risk/Compliance Notes (`risk_notes` / textarea)

## Operational Workflow
1. Record transaction
2. Reconcile balances
3. Audit entry
4. Publish report

## API
- `GET /api/health`
- `GET /api/schema`
- `GET /api/records`
- `POST /api/records`
- `GET /api/metrics`

## Run Locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Docker Run
```bash
docker compose up --build
```

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
