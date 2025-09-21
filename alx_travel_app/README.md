# Property Booking API

A Django REST API for managing property rentals, bookings, and reviews in Kenya - similar to Airbnb.

## Features

- **Property Management**: Create and manage rental properties across Kenya
- **User Bookings**: Book properties with date validation and conflict prevention
- **Review System**: Rate and review properties after completed stays
- **Data Seeding**: Generate sample Kenyan property data for testing

## Models

- **Property**: Rental listings with host, location, price in KES, and details
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

# Create sample Kenyan property data
python manage.py populate_db

# Create admin user (optional)
python manage.py createsuperuser

# Run server
python manage.py runserver
```

## Sample Data

The seeder creates realistic Kenyan properties including:
- **Locations**: Nairobi, Mombasa, Maasai Mara, Lake Naivasha, Lamu, etc.
- **Property types**: Beach houses, safari lodges, city apartments, tea estate bungalows
- **Pricing**: KES 3,000 - 25,000 per night
- **Bookings & Reviews**: Realistic booking patterns and guest reviews

## Seeder Options

```bash
# Basic seeding
python manage.py populate_db

# Custom data counts
python manage.py populate_db --users 15 --properties 30 --bookings 50 --reviews 40

# Clear and reseed
python manage.py populate_db --clear
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

*Built with Django REST Framework for the Kenyan market*