# WASHKING Invoice Management System

```text
WASHKING_invoice_fullstack/
├── backend/
│   ├── main.py
│   ├── config.py
│   ├── database.py
│   ├── schemas.py
│   ├── requirements.txt
│   ├── routes/
│   │   ├── customers.py
│   │   ├── invoices.py
│   │   └── dashboard.py
│   └── services/
│       ├── common.py
│       ├── customer_service.py
│       ├── invoice_service.py
│       └── history_service.py
└── frontend/
    └── index.html
```

Run the API from this folder with:

```bash
pip install -r backend/requirements.txt
uvicorn backend.main:app --reload
```

Open `frontend/index.html` after the API starts.
