
---

# Django REST API

Welcome to the Django REST API project repository! This project demonstrates how to build and deploy a RESTful API using Django and Django REST framework.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This project is designed to provide a robust and scalable RESTful API using Django and Django REST framework. It includes user authentication, CRUD operations, and other common functionalities needed for a REST API.

## Features
- User Authentication (Register, Login, Logout)
- CRUD operations for managing resources
- JWT token-based authentication
- Pagination, Filtering, and Search functionality
- Comprehensive API documentation with Swagger and ReDoc

## Installation
To set up the project locally, follow these steps:

### Prerequisites
- Python 3.7+
- Django 3.x
- Django REST framework
- Docker

### Clone the Repository
```sh
git clone https://github.com/Usama-zia/django_rest_api.git
cd django_rest_api
```

### Set Up a Virtual Environment
It's recommended to create a virtual environment for the project:
```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### Install Dependencies
Install the required dependencies using `pip`:
```sh
pip install -r requirements.txt
```

### Apply Migrations
Apply the database migrations:
```sh
python manage.py migrate
```

### Create a Superuser
Create a superuser to access the Django admin panel:
```sh
python manage.py createsuperuser
```

### Run the Server
Start the development server:
```sh
python manage.py runserver
```

## Usage
Once the server is running, you can access the API at `http://localhost:8000/api/`. Use tools like Postman or cURL to interact with the API endpoints.

### Authentication
- Register: `POST /api/auth/register/`
- Login: `POST /api/auth/login/`
- Logout: `POST /api/auth/logout/`

### CRUD Operations
- Create: `POST /api/items/`
- Read: `GET /api/items/`
- Update: `PUT /api/items/{id}/`
- Delete: `DELETE /api/items/{id}/`

### Example cURL Requests
- **Register**
```sh
curl -X POST http://localhost:8000/api/auth/register/ \
-H "Content-Type: application/json" \
-d '{"username": "user1", "password": "password123"}'
```
- **Login**
```sh
curl -X POST http://localhost:8000/api/auth/login/ \
-H "Content-Type: application/json" \
-d '{"username": "user1", "password": "password123"}'
```

## API Endpoints
Here's a list of available API endpoints:

### Authentication
- `POST /api/auth/register/` - Register a new user
- `POST /api/auth/login/` - Login a user
- `POST /api/auth/logout/` - Logout a user

### Items
- `GET /api/items/` - List all items
- `POST /api/items/` - Create a new item
- `GET /api/items/{id}/` - Retrieve a specific item
- `PUT /api/items/{id}/` - Update a specific item
- `DELETE /api/items/{id}/` - Delete a specific item

### Users
- `GET /api/users/ - Get a list of all users
- `GET /api/users/{id}/ - Get details of a specific user
- `PUT /api/users/{id}/ - Update user details
- `DELETE /api/users/{id}/ - Delete a user

### Example Resource
- `GET /api/resource/ - Get a list of all resources
- `POST /api/resource/ - Create a new resource
- `GET /api/resource/{id}/ - Get details of a specific resource
- `PUT /api/resource/{id}/ - Update resource details
- `DELETE /api/resource/{id}/ - Delete a resource  

## License
Distributed under the MIT License. See `LICENSE` for more information.

---
