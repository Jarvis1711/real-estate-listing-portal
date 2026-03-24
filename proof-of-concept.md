# Proof of Concept - Real Estate Listing Portal

## Scope
- App category: FinTech
- Entity model: Real Estate Ledger Entry
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Account/Wallet: `account_or_wallet` (text)
- Amount: `amount` (number)
- Risk/Compliance Notes: `risk_notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"reconciled","payload":{"account_or_wallet":"Demo value","amount":12,"risk_notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 70
- Generated UTC: 2026-03-24T15:52:22.280036+00:00
- Status: Phase-2 complete
