<div align="center">

  <h1>📚 Digilibzx - Digital Library Management System</h1>

  ![Digilibz Banner](https://img.shields.io/badge/Digilibz-Digital%20Library-blue?style=for-the-badge)
  ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
  ![Next.js](https://img.shields.io/badge/Next.js-black?style=for-the-badge&logo=next.js&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
  ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

**Digilibz** merupakan solusi sistem manajemen perpustakaan digital fullstack yang komprehensif dan modern, dikembangkan dengan integrasi teknologi Java Spring Boot yang tangguh di sisi backend serta Next.js yang responsif di sisi frontend untuk menghadirkan pengalaman pengguna yang mulus dan cepat. Dirancang khusus untuk mentransformasi operasional perpustakaan di lingkungan akademik maupun publik menjadi ekosistem digital yang efisien, sistem ini tidak hanya menyederhanakan proses sirkulasi utama seperti peminjaman dan pengembalian buku secara otomatis, tetapi juga memperkaya interaksi pengguna melalui fitur ulasan, notifikasi real-time, dan ringkasan berbasis AI, sekaligus membekali administrator dengan dashboard statistik analitik untuk pengelolaan inventaris dan pemantauan aktivitas perpustakaan yang lebih transparan, terstruktur, dan terukur dalam satu platform terpadu.

</div>





##  Fitur Utama

### 👤 User 
* **Pencarian Cerdas:** Cari buku berdasarkan judul, kategori, atau penulis.
* **Sirkulasi Mandiri:** Melakukan peminjaman (Borrow) dan melihat estimasi pengembalian.
* **Riwayat Transaksi:** Memantau status peminjaman (Pending, Dipinjam, Dikembalikan, Terlambat).
* **Sistem Review:** Memberikan ulasan dan rating pada buku yang telah dibaca.
* **Notifikasi Real-time:** Mendapatkan pemberitahuan status peminjaman.
* **Fitur AI:** Ringkasan buku otomatis (AI Summarize).

### 🛠 Admin
* **Dashboard Statistik:** Visualisasi data peminjaman, buku populer, dan aktivitas pengguna.
* **Manajemen Buku:** Tambah, edit, dan hapus data buku (termasuk upload cover).
* **Manajemen User:** Mengelola akun pengguna (Admin, Dosen, Mahasiswa).
* **Approval Peminjaman:** Menyetujui atau menolak permintaan peminjaman buku.
* **Manajemen Pengembalian:** Memproses pengembalian buku dan denda keterlambatan.

---

<br>

## 🛠️ Tech Stack

### Backend
* **Framework:** Java Spring Boot 3.x
* **Language:** Java 17+
* **Database:** MySQL
* **Security:** Spring Security & JWT Authentication
* **Build Tool:** Maven

### Frontend
* **Framework:** Next.js 14/15 (App Router)
* **Language:** TypeScript
* **Styling:** Tailwind CSS & Shadcn UI
* **State Management:** React Hooks
* **Package Manager:** pnpm / npm

---

<br>

## 📂 Struktur Proyek

```text
root/
├── backend/            # Source code Backend (Spring Boot)
│   ├── src/main/java   # Controllers, Services, Repositories, Models
│   └── src/main/resources
│       └── db/         # SQL Backup (backup.sql)
├── frontend/           # Source code Frontend (Next.js)
│   ├── app/            # Pages & Routing
│   ├── components/     # Reusable UI Components
│   └── lib/            # API Helper Functions
└── document/           # Dokumentasi Proyek (API Docs, ERD, SRS)

```

<br>

---

## ⚙️ Cara Instalasi & Menjalankan

Ikuti langkah-langkah berikut untuk menjalankan proyek di lokal komputer Anda.

### 1. Persiapan Database

1. Pastikan **MySQL** sudah berjalan.
2. Buat database baru bernama `digilibz_db` (atau sesuaikan dengan konfigurasi Anda).
3. Import file database awal yang terletak di:
`backend/src/main/resources/db/backup.sql`

### 2. Konfigurasi Backend (Spring Boot)

1. Buka folder `backend` di IDE (IntelliJ IDEA / VS Code).
2. Buka file `src/main/resources/application.properties` (atau `.yml`).
3. Sesuaikan konfigurasi database Anda:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/digilibz_db
spring.datasource.username=root
spring.datasource.password=password_mysql_anda

# JWT Configuration
jwt.secret=masukkan_secret_key_yang_panjang_dan_aman_disini
jwt.expiration=86400000

```


4. Jalankan aplikasi dengan perintah:
```bash
mvn spring-boot:run

```


*Backend akan berjalan di port `8080`.*

### 3. Konfigurasi Frontend (Next.js)

1. Buka terminal baru dan masuk ke folder `frontend`.
```bash
cd frontend

```


2. Install dependencies:
```bash
pnpm install
# atau jika menggunakan npm:
npm install

```


3. Buat file `.env.local` di dalam folder `frontend` dan tambahkan:
```env
NEXT_PUBLIC_API_URL=http://localhost:8080/api

```


4. Jalankan server frontend:
```bash
pnpm dev
# atau
npm run dev

```


*Frontend akan berjalan di `http://localhost:3000`.*

<br>

---

## 📝 Dokumentasi API

Dokumentasi lengkap mengenai endpoint API dapat ditemukan di folder `document/`:

* [API Documentation](https://www.google.com/search?q=document/DocsApi.md)

<br>

## 📄 Lisensi

Didistribusikan di bawah Lisensi MIT. Lihat `LICENSE` untuk informasi lebih lanjut.

