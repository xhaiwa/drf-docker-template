# DRF Docker Template

A starter template for building Django REST Framework (DRF) projects with Docker.

## Features

- Django & Django REST Framework pre-configured
- Docker & Docker Compose setup for local development
- PostgreSQL database integration
- Environment variable support via `.env`
- Ready for production deployment

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)

### Setup

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/drf-docker-template.git
    cd drf-docker-template
    ```

2. **Copy environment variables:**
    ```bash
    cp .env.example .env
    ```

3. **Build and start the containers:**
    ```bash
    docker-compose up --build
    ```

4. **Apply migrations and create a superuser:**
    ```bash
    docker-compose exec web python manage.py migrate
    docker-compose exec web python manage.py createsuperuser
    ```

5. **Access the app:**
    - API: [http://localhost:8000/](http://localhost:8000/)
    - Admin: [http://localhost:8000/admin/](http://localhost:8000/admin/)

## Project Structure

```
drf-docker-template/
├── app/                # Django project code
├── Dockerfile
├── docker-compose.yml
├── .env.example
└── README.md
```

## Customization

- Update dependencies in `requirements.txt`
- Add your DRF apps in the `app/` directory

## License

MIT License