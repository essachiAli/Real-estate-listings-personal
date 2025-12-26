## 1. Install Production Dependencies

(Usually done on the server)

```bash
composer install --optimize-autoloader --no-dev
```

**Why**

* Installs only production packages
* Optimizes class loading for better performance

---

## 2. Environment Configuration

```bash
cp .env.example .env
```

Then generate the application key:

```bash
php artisan key:generate
```

**Why**

* `.env` holds environment-specific values (DB, mail, cache)
* `APP_KEY` is required for encryption and sessions

---

## 3. Cache Configuration (VERY IMPORTANT)

```bash
php artisan config:clear
php artisan config:cache
```

**Why**

* Clears old config
* Combines config files into one cached file (faster)

---

## 4. Optimize Routes

```bash
php artisan route:clear
php artisan route:cache
```

**Why**

* Caches routes for better performance
* Required for production environments

⚠️ **Note:** Route caching works only if you don’t use closures in routes.

---

## 5. Optimize Views

```bash
php artisan view:clear
php artisan view:cache
```

**Why**

* Pre-compiles Blade templates
* Faster page rendering

---

## 6. Clear and Cache Events (Laravel 9+)

```bash
php artisan event:clear
php artisan event:cache
```

**Why**

* Optimizes event/listener loading

---

## 7. Run Database Migrations

```bash
php artisan migrate --force
```

**Why**

* Applies database changes in production
* `--force` bypasses confirmation prompt

---

## 8. Optimize the Application (One Command)

```bash
php artisan optimize
```

**What it does**

* Caches config
* Caches routes
* Optimizes framework bootstrap files

---

## 9. Set Correct Permissions (Linux Hosting)

```bash
chmod -R 775 storage bootstrap/cache
```

**Why**

* Laravel needs write access for logs, cache, and sessions

---

## 10. (Optional) Queue & Cache Setup

```bash
php artisan queue:restart
php artisan cache:clear
```

**Why**

* Restarts queue workers
* Clears old cached data

---

## 🔑 Final “Production Ready” Checklist Command Set

```bash
composer install --optimize-autoloader --no-dev
php artisan key:generate
php artisan migrate --force
php artisan optimize
php artisan view:cache
```

---
