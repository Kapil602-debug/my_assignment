# Event Manager (Django + React)

A web app where admins can add events via Django admin panel, and events display automatically on a React frontend.

## Features
- **Admin Panel**: Add/edit events in Django admin
- **React Frontend**: Displays all events in real-time
- **API Connection**: React fetches data from Django

## Setup Instructions

### 1. Backend (Django)
```bash
# Install requirements
pip install django djangorestframework django-cors-headers

# Run migrations
python manage.py migrate

# Create superuser (admin account)
python manage.py createsuperuser

# Start server
python manage.py runserver



Access admin at: http://127.0.0.1:8000/admin

API endpoint: http://127.0.0.1:8000/api/events/


project/
├── eventmanager/      # Django backend
│   ├── settings.py    # CORS and app config
│   └── urls.py        # API routes
├── events/            # Django app
│   ├── models.py      # Event model
│   └── admin.py       # Admin panel setup
└── event-display/     # React frontend
    └── src/App.js     # Main component
