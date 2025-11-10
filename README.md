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

## 🖼️ Project Screenshots

Below are the key pages of the **E-commerce Interior Design Webstore** project.

---

### 🔐 Login Page
Here’s how the login page looks — clean, simple, and user-friendly.

![Login Page](C:\Users\user\OneDrive\Pictures\login.png)

---

### 📊 Dashboard Page
After logging in, users/admins are directed to the dashboard where they can manage and view details.

![Dashboard](C:\Users\user\OneDrive\Pictures\dashboard.png)

---

## 📁 Folder Structure




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


## 🔒 Authentication Flow

The **E-commerce Interior Design Webstore** includes a secure and user-friendly authentication system built with Django’s authentication framework.

### 👤 User Actions

1. **Signup / Registration**
   - New users can create an account through the **Signup Page**.
   - The registration form collects essential details such as username, email, and password.
   - Once registered successfully, the user is automatically redirected to the **Login Page**.

2. **Login**
   - Registered users can log in using their credentials.
   - Upon successful login, users are redirected to the **Home Page**, where they can browse products, add them to the cart, and proceed to checkout.

3. **Logout**
   - A **Logout** button appears on the **top-right corner of the header** once the user is logged in.
   - Clicking on it securely logs out the user and redirects them to the **Login Page**.

4. **Access Control**
   - Certain pages like the **Cart** and **Checkout** are only accessible to authenticated users.
   - If a non-logged-in user tries to access these pages, they are automatically redirected to the **Login Page**.

---

### 🧑‍💼 Admin Authentication

- Admin users can log in through the **Django Admin Panel** at:
  👉 [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)
- Admins can:
  - Manage users
  - Add/edit/delete products
  - Manage categories
  - Monitor customer orders

---

### ⚙️ Security Highlights

- Passwords are stored in a **hashed format** (never in plain text).
- Built-in Django authentication ensures CSRF protection, session handling, and secure login.
- Logout endpoints automatically clear user sessions to prevent unauthorized access.

---

### 🔁 User Flow Summary

| Step | Action | Redirect |
|------|---------|-----------|
| 📝 Signup | User registers a new account | Redirects to Login Page |
| 🔐 Login | User enters credentials | Redirects to Home Page |
| 🛍️ Authenticated Access | User can browse, add to cart, and checkout | Stay on Home/Cart |
| 🚪 Logout | User clicks logout | Redirects to Login Page |

---

✨ This ensures a smooth, secure, and intuitive authentication experience for all users — keeping the app both functional and safe.


## 💡 Future Enhancements

This project can be further expanded with the following advanced features and improvements:

### 🧾 1. Payment Gateway Integration
- Integrate **Stripe**, **PayPal**, or **Razorpay** for secure online payments.  
- Enable multiple payment options such as credit/debit cards, UPI, and wallets.

### 🚚 2. Order Management & Tracking
- Implement an **order tracking system** for users to check their order status in real-time.  
- Add an admin dashboard for managing order history, returns, and refunds.

### 💬 3. Product Reviews & Ratings
- Allow users to submit reviews and star ratings for products.  
- Display average ratings and user feedback on the product detail page.

### 🌍 4. Multi-Language & Currency Support
- Add **internationalization (i18n)** for multi-language support.  
- Provide currency conversion options based on the user’s region.

### 📱 5. Responsive UI & Mobile Optimization
- Redesign the front-end using modern UI frameworks like **Bootstrap 5** or **Tailwind CSS**.  
- Ensure the site is fully responsive across all devices.

### 🔔 6. Email & Notification System
- Send **order confirmation**, **shipping updates**, and **password reset** emails.  
- Use background task queues like **Celery** for handling notifications efficiently.

### 📦 7. Wishlist & Recently Viewed Products
- Add a **wishlist** feature for saving favorite products.  
- Display **recently viewed items** to enhance user experience.

### 🧠 8. AI-Powered Recommendations
- Suggest products based on user preferences and browsing history.  
- Use basic machine learning models for personalized recommendations.

### 🔐 9. Enhanced Security
- Implement **two-factor authentication (2FA)** for user accounts.  
- Use **reCAPTCHA** during registration to prevent bot signups.

### 🧰 10. Deployment & Scalability
- Deploy the app on cloud platforms like **AWS**, **Azure**, or **Heroku**.  
- Use Docker and Nginx for scalability and production readiness.

---

🚀 *These improvements will help transform this e-commerce website into a fully featured, secure, and scalable online shopping platform.*


## 👨‍💻 Developer

### 👤 **Sai Varun**
**Full Stack Python Developer**

💡 Passionate about building dynamic, user-friendly, and scalable web applications using **Django**, **Python**, and **modern front-end technologies**.

📍 Skilled in:
- Django | Python | HTML | CSS | JavaScript | Bootstrap  
- SQL | SQLite | REST APIs | Git & GitHub  
- Full Stack Web Development | Responsive UI Design

📫 **Contact Information:**
- 📧 Email: [saivarunvarun@gmail.com](mailto:saivarunvarun@gmail.com)
- 🌐 GitHub: [github.com/Saivarunvarun](https://github.com/Saivarunvarun)
- 💼 LinkedIn: *(Add your LinkedIn link here if you have one)*

🧠 **About Me:**
> I enjoy designing and developing web solutions that solve real-world problems.  
> My focus is on writing clean, maintainable code and delivering visually appealing and efficient applications.

⭐ *If you like this project, please star it on GitHub — your support means a lot!*

