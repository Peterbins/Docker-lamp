# 🚀 Docker LAMP Stack

A complete LAMP stack running in Docker with **PHP 8.4**,
**MySQL/MariaDB**, **phpMyAdmin**, and **MailHog** for email testing.

## 📦 Stack Contents

### **PHP 8.4** includes:

-   imagick
-   pdo_mysql
-   pdo_sqlite
-   bcmath
-   mysqli
-   curl
-   zip
-   mbstring
-   gettext
-   calendar
-   exif
-   soap
-   freetype

### Additional services:

-   **Apache 2**
-   **MySQL or MariaDB** (latest)
-   **phpMyAdmin**
-   **MailHog** (captures outgoing emails)
-   Persistent volumes for data and logs

## ✉️ Email Testing with MailHog

MailHog captures all outgoing emails inside Docker.

### **PHPMailer SMTP configuration**

``` php
$mail->isSMTP();
$mail->Host = 'mailhog';   // Docker service name
$mail->Port = 1025;
$mail->SMTPAuth = false;
$mail->SMTPSecure = false;
```

View captured emails at:\
👉 http://localhost:8025

## 🛠 Installation

``` bash
git clone https://github.com/Peterbins/Docker-lamp.git
cd Docker-lamp/
sudo docker compose up -d
```

## 🌐 Service URLs

  Service      URL
  ------------ -----------------------
  Website      http://localhost
  phpMyAdmin   http://localhost:8080
  MailHog      http://localhost:8025

## 🔄 Start / Stop Commands

### Stop the stack

``` bash
docker compose down
```

### Start the stack

``` bash
docker compose up -d
```

### Rebuild containers

``` bash
docker compose up -d --build
```

## 📁 Project Structure

    Docker-lamp/
    │
    ├── bin/
    │   ├── webserver/       # PHP + Apache build
    │   └── mysql/           # Database engine build
    │
    ├── config/
    │   ├── php/             # php.ini
    │   └── vhosts/          # Apache VirtualHosts
    │
    ├── data/                # Persistent database files
    ├── logs/                # Apache & MySQL logs
    └── www/                 # Public web root

## ℹ️ Additional Information

-   MailHog does **not** send real emails --- all messages are captured
    locally.
-   Perfect for development, testing, and local PHP/LAMP projects.
