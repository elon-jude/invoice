# WASHKING Invoice Backend

## Structure

- `main.py` - FastAPI application entry point
- `config.py` - application/database configuration
- `database.py` - SQLite connection and schema initialization
- `schemas.py` - request validation models
- `routes/` - API endpoints
- `services/` - business logic
- `invoices.db` - generated SQLite database (created on first run)

## Run

From the project root:

```bash
pip install -r backend/requirements.txt
uvicorn backend.main:app --reload
```

API docs: `http://localhost:8000/docs`

The frontend is in `frontend/index.html` and expects the API at `http://localhost:8000`.

## Invoice history

Every invoice keeps a chronological audit trail in `invoice_history`. Events include `INVOICE_CREATED`, `PAYMENT_RECORDED`, and `INVOICE_PAID`.

Useful endpoints:

- `GET /invoices/{invoice_id}` - complete invoice, customer, payments and history
- `GET /invoices/{invoice_id}/history` - invoice history only
- `GET /customers/{customer_id}/history` - all invoices belonging to a customer
