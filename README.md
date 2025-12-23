# Digilibz - Digital Library Management System

**Digilibz** adalah platform perpustakaan digital modern yang dirancang untuk mempermudah pengelolaan koleksi buku, transaksi peminjaman, serta interaksi antara pengguna dan administrator. Dengan antarmuka yang ramah pengguna dan fitur canggih, Digilibz memungkinkan mahasiswa dan dosen untuk mengakses buku dengan mudah, memberikan ulasan, dan mendapatkan rekomendasi buku berbasis AI. Untuk administrator, Digilibz menyediakan alat yang efisien untuk mengelola buku, pengguna, dan transaksi, membuat manajemen perpustakaan lebih terorganisir dan otomatis.

## 🚀 Teknologi yang Digunakan

Proyek ini dibangun menggunakan arsitektur *monorepo* (backend dan frontend dalam satu repositori) dengan *tech stack* berikut:

### Backend
* **Language:** Java
* **Framework:** Spring Boot 3
* **Build Tool:** Maven
* **Database:** SQL (MySQL/PostgreSQL) - *Lihat `backup.sql`*
* **Security:** Spring Security & JWT Authentication
* **Fitur Utama:** REST API, Manajemen Transaksi, Sistem Notifikasi.

### Frontend
* **Framework:** Next.js 14 (App Router)
* **Language:** TypeScript
* **Styling:** Tailwind CSS
* **UI Components:** Shadcn UI
* **Icons:** Lucide React / SVG Assets
* **Package Manager:** pnpm
* **Integrasi AI:** Fitur ringkasan buku otomatis.

---

## ✨ Fitur Utama

### 👤 Pengguna (Mahasiswa/Dosen)
* **Otentikasi:** Register dan Login (Role based).
* **Koleksi Buku:** Mencari, memfilter, dan melihat detail buku.
* **Peminjaman:** Sistem "Keranjang" peminjaman dan pembuatan Invoice peminjaman.
* **Ulasan:** Memberikan rating dan komentar pada buku untuk berbagi opini.
* **Personalisasi:** Bookmark buku dan rekomendasi buku.
* **Riwayat:** Melihat riwayat transaksi peminjaman dan pengembalian.
* **AI Summary:** Mendapatkan ringkasan isi buku menggunakan AI.

### 🛡️ Administrator
* **Dashboard Statistik:** Grafik peminjaman, total buku, dan aktivitas pengguna.
* **Manajemen Buku:** Menambah, mengedit, dan menghapus data buku dengan mudah.
* **Manajemen User:** Mengelola data pengguna (Mahasiswa/Dosen/Admin).
* **Manajemen Transaksi:** memvalidasi peminjaman dan proses pengembalian buku.
* **Laporan:** Memantau status buku dan denda transaksi secara efisien.

---

## 🛠️ Persiapan Instalasi

Pastikan Anda telah menginstal perangkat lunak berikut di komputer Anda:
1.  **Java Development Kit (JDK) 17** atau lebih baru.
2.  **Node.js** (Versi LTS disarankan).
3.  **Maven** (Untuk build backend).
4.  **Database Server** (MySQL atau PostgreSQL).

---

## ⚙️ Panduan Instalasi & Menjalankan Aplikasi

### 1. Setup Database
Sebelum menjalankan backend, impor file database yang tersedia:
1.  Buat database baru di local server Anda (misal: `digilibz_db`).
2.  Import file SQL yang terletak di:
    `backend/src/main/resources/db/backup.sql`

### 2. Menjalankan Backend (Spring Boot)

Buka terminal dan arahkan ke folder `backend`:

```bash
cd backend

```

Konfigurasi koneksi database (jika perlu) pada file `application.properties` (atau buat jika belum ada), lalu jalankan aplikasi:

```bash
# Install dependencies
mvn clean install

# Jalankan aplikasi
mvn spring-boot:run

```

*Backend akan berjalan secara default di port `8080`.*

### 3. Menjalankan Frontend (Next.js)

Buka terminal baru (jangan matikan terminal backend) dan arahkan ke folder `frontend`:

```bash
cd frontend

```

Instal dependensi dan jalankan server pengembangan:

```bash
# Install dependencies menggunakan pnpm (disarankan karena ada pnpm-lock.yaml)
npm install -g pnpm  # Jika pnpm belum terinstall
pnpm install

# Jalankan mode development
pnpm dev

```

*Frontend akan berjalan di `http://localhost:3000`.*

---

## 📂 Struktur Proyek

```
digilibz/
├── backend/                # Source code Spring Boot
│   ├── src/main/java       # Controllers, Services, Models
│   ├── src/main/resources  # Konfigurasi DB, SQL Backup
│   └── pom.xml             # Maven dependencies
├── frontend/               # Source code Next.js
│   ├── app/                # Pages & Routing (App Router)
│   ├── components/         # UI Components (Shadcn)
│   ├── lib/                # API calls & Utilities
│   └── public/             # Assets (Images, Icons)
└── README.md               # Dokumentasi Proyek

```

## 🤝 Kontribusi

Kontribusi selalu diterima! Silakan buat *Pull Request* atau laporkan masalah (issue) jika Anda menemukan *bug*.

## 📄 Lisensi

Proyek ini dilindungi di bawah lisensi yang tercantum dalam file `LICENSE` (Lihat file LICENSE untuk detailnya).

```
