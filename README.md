# Little Lemon API Project

This repository contains the Little Lemon API project developed as part of Meta's Django course on Coursera. The project is a RESTful API built using Python and the Django REST Framework, designed to manage restaurant operations for the Little Lemon restaurant. The API supports functionalities for admins, managers, delivery crew, and customers, enabling tasks such as user management, menu item handling, order processing, and cart operations.

## Project Overview

The Little Lemon API provides a robust backend for restaurant management, allowing different user roles to perform specific tasks. The API is built with Django and Django REST Framework, utilizing token-based authentication for secure access. The project demonstrates skills in developing, securing, and deploying RESTful APIs to meet the needs of a restaurant business.

### Key Functionalities

The API supports the following functionalities, categorized by user role:

#### Admin
1. Assign users to the manager group.
2. Access the manager group with an admin token.
3. Add menu items.
4. Add categories.

#### Managers
5. Log in with credentials.
6. Update the item of the day.
7. Assign users to the delivery crew.
8. Assign orders to the delivery crew.

#### Delivery Crew
9. Access orders assigned to them.
10. Update an order as delivered.

#### Customers
11. Register for an account.
12. Log in using username and password to obtain access tokens.
13. Browse all categories.
14. Browse all menu items at once.
15. Browse menu items by category.
16. Paginate menu items.
17. Sort menu items by price.
18. Add menu items to the cart.
19. Access previously added items in the cart.
20. Place orders.
21. Browse their own orders.

## Setup Instructions

Follow these steps to set up and run the Little Lemon API project locally.

### Prerequisites
- Python 3.8 or higher
- Pipenv (for managing virtual environments and dependencies)
- Git (for cloning the repository)

### Installation

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd LittleLemon
   ```

2. **Set Up the Virtual Environment**:
   - Create and activate a virtual environment using Pipenv:
     ```bash
     pipenv shell
     ```

3. **Install Dependencies**:
   - Install the required packages listed in the `Pipfile`:
     ```bash
     pipenv install
     ```

4. **Apply Database Migrations**:
   - Create and apply migrations to set up the database:
     ```bash
     python manage.py makemigrations
     python manage.py migrate
     ```

5. **Run the Development Server**:
   - Start the Django development server:
     ```bash
     python manage.py runserver
     ```
   - The API will be accessible at `http://127.0.0.1:8000`.

### Creating a Superuser (Admin)
To manage the API as an admin, create a superuser account:
```bash
python manage.py createsuperuser
```
Follow the prompts to set up the username, email, and password. Use these credentials to log in to the Django admin panel at `http://127.0.0.1:8000/admin`.

## Usage

- **Accessing the API**: Use tools like Postman or cURL to interact with the API endpoints. Most endpoints require authentication via token, which can be obtained by logging in as a customer or manager.
- **Admin Panel**: Admins can access the Django admin interface to manage users, menu items, and categories.
- **Testing Endpoints**: Ensure you have tokens for authenticated endpoints. For example, to browse menu items or place orders, customers must first log in to obtain a token.

## Project Structure

- **`LittleLemon/`**: Root directory containing the Django project settings.
- **`LittleLemonAPI/`**: Contains the API application with models, views, serializers, and URLs.
- **`Pipfile`**: Lists project dependencies for Pipenv.
- **`manage.py`**: Django's command-line utility for administrative tasks.

## Contributing

This project was developed as part of a Coursera peer-reviewed assignment. Contributions are not expected, but feedback is welcome. If you encounter issues or have suggestions, please open an issue in the repository.

## Acknowledgments

This project was completed as part of Meta's Django course on Coursera. Special thanks to the course instructors and peers for their guidance and feedback during the development and review process.
