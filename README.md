# Online Bookstore - IT1100 IWT Final Project

A full-stack web application for managing and purchasing books online, built with PHP, MySQL, and Bootstrap.

## 📋 Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [User Roles](#user-roles)
- [Database](#database)
- [File Descriptions](#file-descriptions)
- [Technologies Used](#technologies-used)

## ✨ Features

### Core Functionality
- **User Authentication**: Secure login system for admins and authors
- **Book Management**: Add, view, update, and delete books from the catalog
- **Author Management**: Dedicated author portal with dashboard
- **User Accounts**: User registration and profile management
- **Shopping Cart & Orders**: Book ordering and order management
- **Feedback & Reviews**: Customer feedback system with view and update capabilities
- **Blog**: Content creation and management for blog posts
- **FAQ**: Frequently asked questions page
- **Contact Us**: Customer contact form
- **About Us**: Company information page

### User Features
- Browse book catalog
- View author information
- Read blog posts
- Submit feedback and reviews
- Place orders
- Manage user account

### Admin Features
- Manage all books
- View all users
- Monitor feedback and reviews
- Dashboard access

### Author Features
- Manage author profile
- View author dashboard
- Access dedicated author portal

## 📁 Project Structure

```
Online Bookstore (academic project)/
├── CSS/                          # Stylesheets
│   ├── author_dashboard.css
│   ├── blog.css
│   ├── FAQ.css
│   ├── footer.css
│   ├── header_oluwa.css
│   └── [other CSS files]
├── js/                           # JavaScript files
│   ├── author.js
│   ├── bookScript.js
│   ├── myScript.js
│   └── [other JS files]
├── images/                       # Image assets
│   ├── homecover1.avif
│   ├── brownback.jpg
│   └── [other images]
├── styles/                       # Additional stylesheets
│   ├── styles.css
│   ├── stylesoluwa.css
│   └── [other style files]
├── config.php                    # Database configuration
├── login.php                     # User login logic
├── header_oluwa.php             # Header component
├── footer.php                   # Footer component
├── [Feature-specific files]
└── README.md                    # This file
```

## 🔧 Prerequisites

- **PHP** 7.0 or higher
- **MySQL** 5.7 or higher
- **Web Server** (Apache, Nginx, or built-in PHP server)
- **Browser** with JavaScript enabled

## 📦 Installation

### 1. Setup Database
```bash
# Create a new MySQL database
CREATE DATABASE bookstore_database;
```

### 2. Import Database Tables
Create the necessary tables in your `bookstore_database`. The application expects tables for:
- users
- books
- authors
- orders
- feedback
- blog_posts

### 3. Configure Database Connection
Edit `config.php` and update the database credentials:
```php
$con = new mysqli("localhost", "root", "", "bookstore_database");
```

### 4. Deploy Files
- Copy all project files to your web server's root directory (typically `/htdocs` for XAMPP or `/var/www/html` for Linux)

### 5. Start Web Server
If using XAMPP:
- Start Apache and MySQL services

If using PHP's built-in server:
```bash
php -S localhost:8000
```

## ⚙️ Configuration

### Database Configuration (`config.php`)
Update the following variables with your database credentials:
- **Host**: localhost
- **Username**: root
- **Password**: (empty by default)
- **Database**: bookstore_database

### Login Credentials (Default)

| Role   | Email                | Password |
|--------|----------------------|----------|
| Admin  | admin@gmail.com      | admin    |
| Author | author@gmail.com     | author   |

**⚠️ Important**: Change these credentials before deploying to production!

## 🚀 Usage

### For Regular Users
1. Visit the homepage (`index.php` or main entry point)
2. Browse available books
3. Create an account or login
4. Place orders
5. Submit feedback and reviews
6. View your account details

### For Authors
1. Login with author credentials
2. Access author dashboard (`author_dashboard.php`)
3. Manage your author profile
4. View your published books

### For Admins
1. Login with admin credentials
2. Access user display page (`display.php`)
3. Manage books and users
4. Monitor feedback and reviews

## 👥 User Roles

### Admin
- Full system access
- Manage all books and users
- View and manage feedback
- Access dashboard

### Author
- Dedicated portal access
- Profile management
- View assigned books
- Access author-specific features

### Regular User
- Browse catalog
- Place orders
- Submit feedback
- Manage profile

## 🗄️ Database

The application requires the following database tables:

| Table | Purpose |
|-------|---------|
| users | Store user account information |
| books | Store book details and inventory |
| authors | Store author information |
| orders | Store customer orders |
| feedback | Store user reviews and feedback |
| blog_posts | Store blog content |

**Database Name**: `bookstore_database`

## 📄 File Descriptions

### Entry Points
- `login.php` - User authentication and login handling
- `main_sara.php` - Main book listing page
- `index.php` - Homepage

### User Management
- `submitUser.php` - User registration processing
- `display_userdetail.php` - Display user information
- `display.php` - Admin user management page
- `user_Acc.php` - User account management

### Book Management
- `create_sara.php` - Create new book entry
- `read_sara.php` - Read/view book details
- `update.php` - Update book information
- `delete.php` - Delete book record
- `new.php` - New book form

### Author Management
- `author_create.php` - Create author profile
- `author_dashboard.php` - Author portal dashboard
- `author_update.php` - Update author information
- `author_delete.php` - Delete author account

### Additional Features
- `feedback.php` - Feedback submission form
- `view_feedback.php` - View all feedback
- `update_feedback_process.php` - Update feedback
- `delete_feedback.php` - Delete feedback
- `blog_sara.php` - Blog page
- `blog process_sara.php` - Blog processing
- `FAQ_sara.php` - FAQ page
- `about us_gimhani.php` - About page
- `contact us_gimhani.php` - Contact page
- `terms_sara.php` - Terms of service

### Utilities
- `header_oluwa.php` - Reusable header component
- `footer.php` - Reusable footer component
- `config.php` - Database configuration
- `connect_sara.php` - Database connection wrapper

## 🛠️ Technologies Used

- **Backend**: PHP 7.0+
- **Database**: MySQL 5.7+
- **Frontend**: HTML5, CSS3, Bootstrap 5.3.3
- **JavaScript**: Vanilla JavaScript
- **HTTP Server**: Apache/Nginx

## 📝 Notes

- This is an academic project for IT1100 - Internet Web Technologies course
- Default login credentials should be changed before production deployment
- Ensure proper file permissions are set on the web server
- Regularly backup the database
- Consider implementing password hashing and better authentication mechanisms for production use

## 🐛 Troubleshooting

### Database Connection Error
- Verify MySQL is running
- Check database credentials in `config.php`
- Ensure the `bookstore_database` exists

### Login Issues
- Verify correct email and password combination
- Check that default credentials haven't been modified (if applicable)
- Review browser console for JavaScript errors

### Missing Pages
- Ensure all files are properly uploaded to the web server
- Check file permissions
- Verify the web server can access all PHP files




