# Little Lemon Restaurant

A full-stack Django application for the Little Lemon restaurant, featuring a robust Menu API and a Table Booking system with secure authentication.

## Features

- **Menu API**: Browse, search, and manage restaurant menu items.
- **Table Booking**: Secure table reservation system using Django REST Framework ViewSets.
- **User Authentication**: Complete registration, login, and logout functionality powered by Djoser and Token Authentication.
- **Secured Endpoints**: Booking operations are restricted to authenticated users.
- **Unit Tested**: Includes comprehensive tests for models and views.

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd little-lemon
   ```

2. **Set up the virtual environment**:
   ```bash
   python -m venv .venv
   # Windows
   .\.venv\Scripts\activate
   # macOS/Linux
   source .venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install django djangorestframework djoser
   ```

4. **Run migrations**:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Start the server**:
   ```bash
   python manage.py runserver
   ```

## API Endpoints

### Authentication
- `POST /auth/users/`: Register a new user.
- `POST /auth/token/login/`: Obtain an authentication token.
- `POST /auth/token/logout/`: Log out (requires token).

### Menu
- `GET /restaurant/menu/`: List all menu items.
- `POST /restaurant/menu/`: Add a new menu item.
- `GET /restaurant/menu/<id>`: Retrieve a specific item.
- `PUT/PATCH/DELETE /restaurant/menu/<id>`: Update or delete an item.

### Booking (Secured)
- `GET /restaurant/booking/tables/`: List all bookings.
- `POST /restaurant/booking/tables/`: Create a new booking reservation.

## Testing

Run the unit tests with:
```bash
python manage.py test
```
