# Sample Django Project

## Overview

Sample is a production-aware Django project structured using modern best practices.  
It demonstrates:

- Clean project architecture
- Environment-based settings separation
- Secure configuration
- Proper Git discipline
- Production-readiness principles

This project serves as a foundation for scalable Django applications.

---

## Tech Stack

- Python 3.11+
- Django 6.0.2
- SQLite (development)

---

## Project Architecture

```

demo/
│
├── sample/
│   ├── manage.py
│   ├── sample/
│   │   ├── settings/
│   │   │   ├── base.py
│   │   │   ├── development.py
│   │   │   └── production.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   │   └── asgi.py
│
├── requirements.txt
├── .env.example
└── README.md

```

---

## Environment Configuration

Create a `.env` file:

```

DJANGO_SECRET_KEY=your-secret-key

```

---

## Installation

Clone repository:

```

[it clone https://github.com/cherryaugusta/sample.git](git clone https://github.com/cherryaugusta/sample.git)
cd sample

```

Create virtual environment:

```

python -m venv venv
venv/Scripts/activate

```

Install dependencies:

```

pip install -r requirements.txt

```

Apply migrations:

```

python manage.py migrate

```

Create superuser:

```

python manage.py createsuperuser

```

Run development server:

```

python manage.py runserver

```

---

## Admin Panel

Access:

```

[http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

```

Use superuser credentials to log in.

---

## Security Best Practices Implemented

- DEBUG disabled by default
- SECRET_KEY from environment variables
- Settings split for production/development
- Password validators enabled
- ALLOWED_HOSTS enforced in production

---

## Production Deployment Notes

Set environment variable:

```

export DJANGO_SETTINGS_MODULE=sample.settings.production

```

Run production server with your preferred WSGI server.  
(Django’s built-in `runserver` is only for development.)

---

## What This Project Demonstrates

- Understanding of Django architecture
- Knowledge of production deployment patterns
- Clean code organization
- Git version control proficiency
- Secure configuration handling
- Professional documentation standards

---

## Disclaimer

This project is developed strictly for educational purposes and professional portfolio demonstration.  
It is not intended for commercial production use without further security auditing and configuration hardening.

---

## License

MIT License

---
