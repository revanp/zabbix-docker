# Zabbix Docker Compose

Proyek ini menggunakan Docker Compose untuk mengatur dan menjalankan Zabbix dengan PostgreSQL sebagai database. Ini adalah panduan untuk memulai dan menjalankan layanan Zabbix.

## Prerequisites

Sebelum memulai, pastikan Anda memiliki hal-hal berikut:

- [Docker](https://www.docker.com/get-started) terinstal di sistem Anda.
- [Docker Compose](https://docs.docker.com/compose/install/) terinstal di sistem Anda.

## Struktur Proyek

Proyek ini memiliki struktur sebagai berikut:
├── docker-compose.yml
└── README.md

## Menjalankan Proyek

1. **Clone repositori ini** atau unduh file `docker-compose.yml` ke direktori lokal Anda.

2. **Buka terminal** dan navigasikan ke direktori tempat file `docker-compose.yml` berada.

3. **Jalankan perintah berikut untuk memulai layanan:**

   ```bash
   docker-compose up -d
   ```

   Perintah ini akan mengunduh gambar yang diperlukan dan menjalankan kontainer untuk Zabbix, PostgreSQL, dan Zabbix Agent.

4. **Akses Zabbix Web Interface:**

   Setelah semua kontainer berjalan, Anda dapat mengakses antarmuka web Zabbix di [http://localhost:8080](http://localhost:8080).

   - **Username:** Admin
   - **Password:** zabbix

## Menghentikan Proyek

Untuk menghentikan dan menghapus semua kontainer yang berjalan, jalankan:

```bash
docker-compose down
```

## Konfigurasi

File `docker-compose.yml` berisi konfigurasi untuk:

- **zabbix-db:** Kontainer PostgreSQL untuk menyimpan data Zabbix.
- **zabbix-server:** Kontainer server Zabbix.
- **zabbix-web:** Kontainer antarmuka web Zabbix.
- **zabbix-agent:** Kontainer agen Zabbix untuk monitoring.