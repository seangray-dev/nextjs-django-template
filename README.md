# Full Stack Template using Next.js, Django, and PostgreSQL

This repository consists of a full stack application that uses [Next.js](https://nextjs.org/) for the frontend, and Python [Django](https://www.djangoproject.com/) with [Django Rest Framework](https://www.django-rest-framework.org/) for the backend API, all backed by a [PostgreSQL](https://www.postgresql.org/) database.

## The project is organized into two main subfolders:

- `/frontend`: This is a Next.js project bootstrapped with create-next-app using TypeScript & TailWindCSS
- `/backend`: This is a Django project, equipped with Django Rest Framework for creating API endpoints.

## Getting Started

The project runs with two servers: a frontend server for Next.js and a backend server for Django.

### Running the Frontend

- First, navigate to the frontend subfolder and run the Next.js development server:

```bash
cd frontend

npm run dev
# or
yarn dev
# or
pnpm dev
```

- Open http://localhost:3000 with your browser to see the result.

- You can start editing the page by modifying app/page.tsx. The page auto-updates as you edit the file.

- This project uses next/font to automatically optimize and load Inter, a custom Google Font.

### Running the Backend

First update your database settings located in `backend/nextjs_django_test/settings.py`

```py
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_db_name',
        'USER': 'your_postgres_user',
        'PASSWORD': 'your_postgres_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

Now you can migrate your database:

```bash
python manage.py migrate
```

Then, make sure you're in your backend subfolder and run the Django development server:

```bash
cd backend
python manage.py runserver
```

Your Django API will be available at http://localhost:8000.

You can start creating API endpoints by modifying the Django views and URLs.
