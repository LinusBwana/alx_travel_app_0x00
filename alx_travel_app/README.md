# Property Booking API

A Django REST API for managing property rentals, bookings, and reviews - similar to Airbnb.

## Features

- **Property Management**: Create and manage rental properties
- **User Bookings**: Book properties with date validation and conflict prevention
- **Review System**: Rate and review properties after completed stays
- **Data Seeding**: Generate sample data for testing

## Models

- **Property**: Rental listings with host, location, price, and details
- **Booking**: Reservations with dates, pricing, and status tracking
- **Review**: User reviews with ratings (1-5 stars) and comments

## Quick Start

```bash
# Clone and setup
git clone <your-repo-url>
cd property-booking-api
pip install -r requirements.txt

# Database setup
python manage.py migrate

# Create sample data
python manage.py seed

# Run server
python manage.py runserver
```

## API Endpoints

- `GET /api/properties/` - List all properties
- `POST /api/bookings/` - Create a booking
- `GET /api/reviews/` - View property reviews
- And more...

## Tech Stack

- Django 4.x
- Django REST Framework
- PostgreSQL/SQLite
- UUID primary keys

---

*Built with Django REST Framework*