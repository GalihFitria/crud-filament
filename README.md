# 🎛️ Laravel Filament CRUD

Proyek ini adalah implementasi fitur CRUD menggunakan Laravel dan [Filament Admin Panel](https://filamentphp.com/). Dibangun untuk memudahkan pengelolaan data melalui UI admin yang modern dan responsif.

## 🛠️ Teknologi

- Laravel 10+
- Filament Admin Panel
- MySQL / PostgreSQL / SQLite (pilih sesuai kebutuhan)
- TailwindCSS (default dari Filament)
- PHP 8.1+

## 🚀 Fitur

- Dashboard Admin dengan Filament
- CRUD lengkap (Create, Read, Update, Delete)
- Validasi otomatis
- Pencarian dan filter data
- Soft delete (opsional)
- Relasi antar model (opsional)

## 📦 Instalasi

### 1. Clone Repo

```bash
git clone https://github.com/GalihFitria/crud-filament.git
cd crud-filament
```
### 2. Install Depedency

```bash
composer install
```
### 3. Setup .env

```bash
cp .env.example .env
```
### 4. Konfigurasi Database
Edit `.env` dan sesuaikan:

```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_database
DB_USERNAME=root
DB_PASSWORD=
```
### 5. Jalankan Migrasi dan Seeder

```bash
php artisan migrate --seed
```
### 6. Instalasi Filament
```bash
php artisan make:filament-user
```
> Ikuti perintah untuk membuat user admin.

## ✍️ Membuat CRUD
Contoh membuat resource untuk model `Product`:
```bash
php artisan make:filament-resource Product
```
Filament otomatis membuat:
- Resource class
- Form dan Table builder
- Routing ke panel admin

Edit file di `app/Filament/Resources/ProductResource.php` sesuai kebutuhan.

## 🌐 Akses Admin Panel
Jalankan server:
`php artisan serve`

Buka browser: `http://127.0.0.1:8000/admin`

> Login dengan akun yang telah dibuat sebelumnya.
