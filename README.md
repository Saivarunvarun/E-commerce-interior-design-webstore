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
