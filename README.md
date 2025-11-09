# 🛍️ E-Commerce Interior Design Webstore

A complete **E-Commerce website** built using **Django Framework**, featuring user authentication, product catalog, cart system, and admin management dashboard.

---

## ⚙️ Installation & Setup Guide

Follow these steps to set up and run the project locally 👇

### 1️⃣ Create and activate a virtual environment
```bash
python -m venv venv
venv\Scripts\activate    # On Windows
# OR
source venv/bin/activate # On Mac/Linux

## ⚙️ Installation Steps

### 🧩 Install Dependencies
Make sure you have a virtual environment activated before installing the project dependencies.

```bash
pip install -r requirements.txt

## 🗃️ Apply Database Migrations

Once your virtual environment is activated and dependencies are installed, you need to create and apply database migrations.

Migrations are Django’s way of applying changes you make to your models (like creating or updating tables) into your database.

Run the following commands step by step:

```bash
python manage.py makemigrations
python manage.py migrate

### 👑 Create a Superuser (Admin Panel Access)

To access the Django **Admin Dashboard**, you need to create a superuser account.  
This user will have full permissions to manage products, categories, and users.

Run the following command in your project directory (where `manage.py` is located):

```bash
python manage.py createsuperuser

## 🚀 Run the Development Server

Once all dependencies and migrations are set up, start your Django development server with:

```bash
python manage.py runserver

Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).
November 09, 2025 - 18:42:32
Django version 4.x, using settings 'ecommerce.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.

## 📁 Folder Structure

The project is organized as follows:

E-commerce-interior-design-webstore/
│
├── ecommerce/ # Main project configuration (settings, URLs, WSGI, ASGI)
│ ├── init.py
│ ├── asgi.py
│ ├── settings.py
│ ├── urls.py
│ └── wsgi.py
│
├── ecommerceapp/ # Core app for product and category management
│ ├── models.py
│ ├── views.py
│ ├── urls.py
│ ├── admin.py
│ ├── forms.py
│ └── templates/ecommerceapp/
│
├── accounts/ # Handles user registration, login, and logout
│ ├── views.py
│ ├── urls.py
│ ├── forms.py
│ └── templates/accounts/
│
├── cart/ # Shopping cart logic
│ ├── cart.py
│ ├── context_processors.py
│ ├── models.py
│ ├── views.py
│ └── templates/cart/
│
├── searchapp/ # Handles search functionality for products
│ ├── views.py
│ ├── urls.py
│ └── templates/searchapp/
│
├── static/ # CSS, JS, and image assets
│ ├── css/
│ ├── js/
│ └── img/
│
├── templates/ # Shared HTML templates
│ ├── base.html
│ ├── header.html
│ ├── nav.html
│ ├── footer.html
│ ├── category.html
│ ├── product.html
│ └── registration/
│
├── media/ # Uploaded media files (product images, etc.)
│
├── db.sqlite3 # SQLite database (development)
├── manage.py # Django project management script
└── requirements.txt # Python dependencies list


---

### 🧠 Notes:
- `ecommerceapp/` contains core e-commerce logic like displaying products and categories.  
- `accounts/` manages user authentication (signup, login, logout).  
- `cart/` keeps track of items users add to their cart.  
- `searchapp/` adds dynamic search capability to find products easily.  
- `static/` holds all static frontend files like CSS, JS, and images.  
- `templates/` defines reusable UI components shared across the app.  
- `media/` stores uploaded product images dynamically through the admin panel.

---

Would you like me to include **a “Tech Stack Used” section** (e.g., Django, Bootstrap, SQLite, etc.) next to this — so your README looks more detailed and professional on GitHub?

