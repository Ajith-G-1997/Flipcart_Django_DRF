# Flipcart_Django_DRF



# Django E-commerce API

Simple Django backend for an e-commerce platform with models for users (sellers/buyers), products, orders, and order items.

## Models

* **User:** Extends Django's `AbstractUser` with `is_seller` and `is_buyer` fields.
* **Product:** `name`, `description`, `price`, `stock`, `seller` (ForeignKey to `User`).
* **Order:** `buyer` (ForeignKey to `User`), `order_date`, `status`.
* **OrderItem:** `order` (ForeignKey to `Order`), `product` (ForeignKey to `Product`), `quantity`, `price`.

## Setup

1.  Clone repo.
2.  Create virtual environment and install dependencies (`pip install django djangorestframework mysqlclient`).
3.  Configure database in `settings.py`.
4.  Run migrations (`python manage.py migrate`).
5.  Create superuser (`python manage.py createsuperuser`).
6.  Run server (`python manage.py runserver`).

## API

Define your API endpoints in `urls.py` using Django REST Framework.

## Usage

Use tools like Postman to interact with API endpoints (e.g., `/api/products/`, `/api/orders/`).
