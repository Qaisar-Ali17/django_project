# Tweet App

A simple Twitter-like web application built with Django, allowing users to register, login, create tweets with text and optional photos, and manage their own posts.

## Features

- User registration and authentication
- Create tweets with text and optional photo uploads
- View all tweets in a chronological feed
- Edit and delete personal tweets
- Responsive Bootstrap UI with dark theme
- Admin interface for content management

## Tech Stack

- **Backend**: Django 6.0.1
- **Database**: SQLite
- **Frontend**: HTML, Bootstrap 5.3.8
- **Authentication**: Django's built-in auth system

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Qaisar-Ali17/django_project.git
   cd django_project
   ```

2. Install dependencies:
   ```bash
   pip install -r mysite/requirements.txt
   ```

3. Navigate to the project directory:
   ```bash
   cd mysite
   ```

4. Run migrations:
   ```bash
   python manage.py migrate
   ```

5. Create a superuser (optional, for admin access):
   ```bash
   python manage.py createsuperuser
   ```

6. Start the development server:
   ```bash
   python manage.py runserver
   ```

7. Open your browser and visit `http://127.0.0.1:8000/core/`

## Usage

### User Registration
- Visit the registration page to create a new account
- Provide username, email, and password

### Posting Tweets
- Login to your account
- Click "Create Tweet" to post new content
- Add text (up to 200 characters) and optionally upload a photo
- Submit to publish your tweet

### Managing Tweets
- View all tweets on the main feed
- Edit or delete your own tweets using the buttons on your posts

### Admin Panel
- Access `/admin/` with superuser credentials
- Manage users, tweets, and site content

## Project Structure

```
mysite/
├── core/                    # Main application
│   ├── models.py           # Tweet model
│   ├── views.py            # Application logic
│   ├── forms.py            # Tweet and registration forms
│   ├── urls.py             # URL routing
│   ├── templates/          # HTML templates
│   └── migrations/         # Database migrations
├── templates/              # Global templates (layout)
├── static/                 # Static files (CSS, JS, images)
├── media/                  # User-uploaded files
├── mysite/                 # Django project settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── requirements.txt        # Python dependencies
└── manage.py              # Django management script
```

## API Endpoints

- `/core/` - Tweet list (home page)
- `/core/create/` - Create new tweet (login required)
- `/core/<id>/edit/` - Edit tweet (login required, own tweets only)
- `/core/<id>/delete/` - Delete tweet (login required, own tweets only)
- `/core/register/` - User registration
- `/accounts/login/` - User login
- `/accounts/logout/` - User logout
- `/admin/` - Django admin interface

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).
