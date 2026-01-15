# Simple Chat (Django)

A minimal real-time chat project built with **Django** using the **ASGI** interface, runnable locally for development.

---

## Requirements

- Python **3.12+**
- Django **5.1.5**
- pip

> If you plan to run via ASGI (Uvicorn), also install `uvicorn`.

---

## Setup

```bash
git clone <repo_url>
cd sample_chat
```

### Create and activate virtualenv

**macOS / Linux**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows**
```bat
python -m venv venv
venv\Scripts\activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Initialize database

```bash
python manage.py migrate
python manage.py createsuperuser
```

---

## Run the app

### Option A — Django dev server
```bash
python manage.py runserver
```

Open:
- `http://127.0.0.1:8000/chat/`

### Option B — ASGI with Uvicorn
```bash
uvicorn sample_chat.asgi:application --reload --host 127.0.0.1 --port 8000
```

Open:
- `http://127.0.0.1:8000/chat/`

---

## Notes

- Admin panel: `http://127.0.0.1:8000/admin/`
- Default chat route: `/chat/`
