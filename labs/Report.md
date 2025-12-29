# Laravel Deployment on Hostinger  
## Deployment Lab Report

---

## 1. Introduction

This lab focuses on deploying a Laravel web application on **Hostinger shared hosting**.  
Laravel is a popular PHP framework that follows the MVC (Model–View–Controller) architecture and is widely used for building modern web applications.

The goal of this lab is to understand the complete deployment process, including file upload, environment configuration, database setup, and resolving common hosting-related issues.

---

## 2. Objectives

The objectives of this lab are:

- Deploy a Laravel project on Hostinger shared hosting
- Configure the public directory correctly
- Connect the application to a MySQL database
- Secure the application using environment variables
- Verify that the application works in production

---

## 3. Tools and Technologies Used

- **Framework:** Laravel
- **Hosting Provider:** Hostinger
- **Server Type:** Shared Hosting
- **Database:** MySQL
- **Programming Language:** PHP
- **File Management:** Hostinger File Manager
- **Local Environment:** XAMPP / Laravel Artisan

---

## 4. Prerequisites

Before deployment, the following requirements must be met:

- A working Laravel project tested locally
- A Hostinger hosting account
- A domain or subdomain
- PHP version compatible with Laravel (8.1 or higher)
- MySQL database access

---

## 5. Deployment Steps

### 5.1 Uploading the Laravel Project

1. Login to the Hostinger hPanel.
2. Navigate to **Files → File Manager**.
3. Open the `public_html` directory.
4. Upload the Laravel project as a ZIP file.
5. Extract the project files.

---

### 5.2 Configuring the Public Directory

Laravel uses a `public` folder as the web root, while Hostinger serves files from `public_html`.

Steps:
1. Move all files inside `/public` to `public_html`.
2. Keep the remaining Laravel folders outside `public_html`.
3. Edit `index.php` in `public_html`:

```php
require __DIR__.'/../laravel-project/vendor/autoload.php';
$app = require_once __DIR__.'/../laravel-project/bootstrap/app.php';
````
require __DIR__.'/../blog/vendor/autoload.php';
$app = require_once __DIR__.'/../blog/bootstrap/app.php';
---

### 5.3 Creating the Database

1. Go to **Databases → MySQL Databases**.
2. Create:

   * Database name
   * Database user
   * Password
3. Assign the user to the database with full privileges.

---

### 5.4 Environment Configuration (.env)

The `.env` file is configured with production settings:

```env
APP_NAME=Laravel
APP_ENV=production
APP_DEBUG=false
APP_URL=https://yourdomain.com

DB_CONNECTION=mysql
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=database_name
DB_USERNAME=database_user
DB_PASSWORD=database_password
```

---

### 5.5 Application Key Generation

The application key was generated locally using:

```bash
php artisan key:generate
```

The generated key was copied into the `.env` file.

---

### 5.6 File Permissions

The following directories were given proper permissions (755 or 775):

* `storage`
* `bootstrap/cache`

This prevents permission-related server errors.

---

### 5.7 Database Migration

Because SSH access is limited on shared hosting, database migrations were run locally.
The database was then imported into Hostinger using **phpMyAdmin**.

---

## 6. Testing and Verification

After deployment, the following checks were performed:

* Application loads successfully in the browser
* Database connection works correctly
* Pages render without errors
* Forms and CRUD operations function as expected

---

## 7. Common Issues and Solutions

| Issue                     | Cause                      | Solution                              |
| ------------------------- | -------------------------- | ------------------------------------- |
| 500 Internal Server Error | Wrong paths or permissions | Fix `index.php` paths and permissions |
| Blank Page                | APP_DEBUG disabled         | Check logs in `storage/logs`          |
| Database Error            | Incorrect credentials      | Verify `.env` database settings       |

---

## 8. Conclusion

In this lab, a Laravel application was successfully deployed on Hostinger shared hosting.
The deployment process included file upload, environment configuration, database setup, and permission handling.
This lab demonstrates real-world deployment challenges and solutions when working with Laravel in shared hosting environments.

---

## 9. References

* Laravel Documentation: [https://laravel.com/docs](https://laravel.com/docs)
* Hostinger Knowledge Base

````

---

# ✅ `checklist.md`

```md
# Laravel Deployment Checklist (Hostinger)

---

## 🔹 Pre-Deployment
- [ ] Laravel project works locally
- [ ] Correct PHP version selected on Hostinger
- [ ] `.env` file exists
- [ ] APP_KEY generated
- [ ] Database structure ready

---

## 🔹 Database Setup
- [ ] MySQL database created
- [ ] Database user created
- [ ] User assigned to database
- [ ] Credentials added to `.env`

---

## 🔹 File Upload
- [ ] Project uploaded to Hostinger
- [ ] ZIP file extracted successfully
- [ ] Unnecessary files removed

---

## 🔹 Public Directory Configuration
- [ ] `public` folder contents moved to `public_html`
- [ ] Other Laravel folders placed outside `public_html`
- [ ] `index.php` paths updated correctly

---

## 🔹 Environment Configuration
- [ ] APP_ENV set to `production`
- [ ] APP_DEBUG set to `false`
- [ ] APP_URL set correctly
- [ ] Database variables verified

---

## 🔹 Permissions
- [ ] `storage` folder permission set (755 or 775)
- [ ] `bootstrap/cache` permission set

---

## 🔹 Database Migration
- [ ] Migrations run locally OR via SSH
- [ ] Database imported using phpMyAdmin

---

## 🔹 Final Testing
- [ ] Homepage loads correctly
- [ ] Database connection works
- [ ] No 500 errors
- [ ] Logs checked for warnings

---

## ✅ Deployment Complete
````

---

If you want, I can also:

* Convert this into **PDF or DOCX**
* Simplify it for **short lab submission**
* Customize it with **your university name & student info**
* Adapt it for **Real Estate Laravel project** (based on your previous work)

Just tell me 👌
