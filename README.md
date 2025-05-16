# 🐘 Caveman Databases Stack

Bu proje, lokal geliştirme ortamında birden fazla veritabanı (PostgreSQL, MySQL, MongoDB) ile birlikte yönetim arayüzlerini ayağa kaldırmak için hazırlanmış bir Docker Compose yapısıdır.

## 🚀 İçerik

* **PostgreSQL** (`localhost:5432`)
* **MySQL** (`localhost:3307`)
* **MongoDB** (`localhost:27017`)
* **Mongo Express (MongoDB UI)** → [http://localhost:8081](http://localhost:8081)
* **Adminer (Veritabanı Yönetim UI)** → [http://localhost:8080](http://localhost:8080)

## 🔧 Kurulum

### 1. Docker & Docker Compose Gereksinimi

* [Docker Desktop](https://www.docker.com/products/docker-desktop) veya [Orbstack](https://orbstack.dev) yüklü olmalıdır.

### 2. Projeyi Çalıştır

```bash
docker-compose up -d
```

> İlk çalıştırmada gerekli imajlar indirilecektir.

### 3. Servis Durumlarını Kontrol Et

```bash
docker ps
```

### 4. Veritabanı Arayüzleri

| Servis        | URL                                            |
| ------------- | ---------------------------------------------- |
| Adminer       | [http://localhost:8080](http://localhost:8080) |
| Mongo Express | [http://localhost:8081](http://localhost:8081) |

## 💠 Geliştirici Bilgileri

### PostgreSQL

* **Kullanıcı:** `caveman`
* **Parola:** `password`
* **Veritabanı:** `cave`

### MySQL

* **Root Parolası:** `password`

### MongoDB

* **Kullanıcı:** `caveman`
* **Parola:** `password`

## 🩹 Temizlik

Tüm servisleri durdur ve volume'ları temizle:

```bash
docker-compose down -v
```

## 📁 Volume'lar

Veritabanı verileri volume’larda saklanır:

* `postgre-db`
* `mysql-db`
* `mongodb`
* `mongo-express-db`

## 🧠 Notlar

* `adminer` arayüzü üzerinden PostgreSQL ve MySQL’e bağlanabilirsin.
* `mongo-express` ile MongoDB veritabanlarını görüntüleyebilirsin.
* Portlar çakışıyorsa kendi ihtiyaçlarına göre `docker-compose.yml` dosyasını düzenleyebilirsin.
