# FastAPI-JWT-Authentication-Project
This project is a hands-on implementation of an authentication system built using FastAPI. The goal was to understand how real-world backend systems manage users, authentication, and protected routes.

It includes basic user workflows like registration, login, email verification, password recovery, and updating credentials. To make it more practical, a simple article feature is also added where authenticated users can create and view content.

The backend is connected to a PostgreSQL database using asynchronous SQLAlchemy, and Alembic is used to manage database migrations.

Features:
1.User registration and login
2.JWT-based authentication
3.Email verification flow
4.Forgot and reset password functionality
5.Update password for logged-in users
6.Create and fetch articles (protected routes)

Tech Stack:
1.FastAPI
2.PostgreSQL
3.SQLAlchemy (Async)
4.Alembic
5.JWT (Authentication)

Getting Started:
You can run this project either using Docker or by setting it up locally.

Running with Docker:
This is the simpler approach if Docker is already installed.

Create an environment file:

cp .env.example .env
Add your PostgreSQL credentials in the .env file

Start the containers:

docker-compose up -d --build

or

docker compose up -d --build
Running Locally (Without Docker)

If you prefer manual setup:
Update database configuration in:

alembic/env.py
src/core/config.py

Install dependencies:

pip install -r requirements.txt

Run the project:

chmod 755 start.sh
sh start.sh

This script will apply migrations and start the FastAPI server.
