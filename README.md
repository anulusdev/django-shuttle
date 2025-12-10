# Django Shuttle Application 🚍

A smart campus shuttle coordination system built with Django for the Federal University of Technology, Akure (FUTA) Nigeria. The application connects students who need a shuttle urgently during the day or while coming or going for night class with drivers who may not have smartphones, using SMS notifications. It’s designed to make campus transportation more efficient and inclusive.

# 🌍 Problem Statement

On most campuses, students often face:

Long waiting times for shuttles.

Poor coordination between drivers and passengers.

Drivers not knowing where passengers are located.

Technology gaps (many shuttle drivers only use button phones).

This project solves those problems by:

Grouping students by faculty/destination.

Sending SMS notifications to drivers when passengers are ready.

Allowing drivers to stay connected without needing smartphones.

(Future feature) Using speakers installed near shuttle pickup points to announce when a ride request is made.

# ✨ Features

Students can request a shuttle by selecting their faculty or destination.

System groups passengers going in the same direction to save time and resources.

Drivers are notified via Google SMS API, ensuring compatibility with even button phones.

## Admin dashboard for managing:

Shuttle drivers

Student requests

Ride assignments

Future: Voice/speaker notifications near shuttle pickup points for real-time alerts.

# 🛠 Tech Stack

Backend: Django (Python)

Database: PostgreSQL

Frontend: Django Templates (Bootstrap)

SMS Service: Google SMS API

Others: Gunicorn, Docker (optional for deployment)

# ⚡ Installation & Setup

# Clone the repository

git clone https://github.com/anulusdev/django-shuttle/.git
cd django-shuttle


## Create and activate virtual environment

python -m venv venv
source venv/bin/activate  # for Linux/Mac
venv\Scripts\activate     # for Windows


# Install dependencies

pip install -r requirements.txt


Setup environment variables (create .env file)

SECRET_KEY=your-django-secret-key
DEBUG=True
DATABASE_URL=postgres://user:password@localhost:5432/shuttle_db
GOOGLE_SMS_API_KEY=your-google-sms-api-key


## Apply migrations

python manage.py migrate


Run the development server

python manage.py runserver

# 🚀 Usage Guide

## Students

Visit the app, select your faculty, and request a shuttle.

Your request is queued and grouped with others going in the same direction.

## Drivers

Receive SMS notifications when passengers are waiting.

(Future) Speaker system at the bus-stop to announce ride readiness.

## Admin

Login to manage drivers, requests, and trip records.

# 🎯 Problem It Solves

Reduces waiting time for students.

Optimizes shuttle usage (drivers only move when requests are ready).

Bridges the technology divide by supporting button phones.

Enhances communication between students and drivers.

# 🔮 Future Improvements

Add speaker/voice notifications for drivers in shuttle areas.

Mobile app version for students.

Integration with cashless payments (e.g., campus wallet or Paystack).

AI-based ride grouping & routing optimization.

Ride history & analytics for admins.

# 🙌 Acknowledgments

Built for Federal University of Technology, Akure (FUTA).

Google SMS API for communication.

Django community for backend support.

Inspiration: Solving real transport challenges on campus.
