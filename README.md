# Mini Commerce Kampus

Project ini berisi implementasi backend mini commerce kampus yang menggunakan arsitektur microservices. Aplikasi terdiri dari dua service, yaitu `catalog-service` untuk mengelola data produk dan `order-service` untuk mengelola proses pemesanan serta transaksi.

## Prerequisites

Pastikan environment lokal sudah tersedia:

* OS Windows
* Java 17
* PostgreSQL & pgAdmin
* Postman (untuk testing API)

## Database Setup

Project ini menggunakan pola *Database-per-Service*, sehingga perlu membuat dua database terpisah di PostgreSQL melalui pgAdmin:

1. `catalog_db`
2. `order_db`

## Cara Menjalankan

Jalankan `catalog-service` terlebih dahulu karena `order-service` mengambil data produk dari service tersebut saat melakukan validasi.

1. **Jalankan Catalog Service**
   Buka folder `catalog-service` di IDE, lalu jalankan `CatalogServiceApplication.java`. Service akan berjalan di `localhost:8081`.

2. **Jalankan Order Service**
   Buka folder `order-service` di IDE, lalu jalankan `OrderServiceApplication.java`. Service akan berjalan di `localhost:8082`.

*Skema tabel akan dibuat otomatis oleh Hibernate saat aplikasi dijalankan pertama kali.*

## API Testing & Documentation

Dokumentasi API menggunakan OpenAPI (Swagger). Setelah service berjalan, dokumentasi dapat diakses melalui:

* **Catalog API:** http://localhost:8081/swagger-ui.html
* **Order API:** http://localhost:8082/swagger-ui.html

Untuk mencoba alur aplikasi secara end-to-end, import Postman Collection yang sudah disediakan.
