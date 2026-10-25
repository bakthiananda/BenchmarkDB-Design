# 📊 BenchMarkDB (BMDB-V1.0)

> **Aplikasi Monitoring Telemetri & Database Komparasi Performa PC Berbasis Real-World Condition**

Dokumentasi resmi dan repositori proyek untuk mata kuliah **Analisis dan Desain Perangkat Lunak (INF.62.0025)**.

---

## 👥 Identitas Kelompok (Kelompok 3)
* **Bakthi Ananda Harisona** (24343085)
* **Ganeza Pratama** (24343116)
* **Muhammad Lintang Azhuri** (24343062)
* **Dosen Pengampu:** Randi Proska Sandra, S.Pd, M.Sc
* **Institusi:** Universitas Negeri Padang (Departemen Teknik Elektronika - Teknik Informatika)

---

## 🚀 Latar Belakang & Problem Framing
Video benchmark yang tersedia di platform seperti YouTube atau forum online umumnya diuji pada kondisi pengujian yang ideal (ruangan ber-AC, komponen merk kelas atas, *cooler* mahal,dll), sehingga sering kali berbeda dengan performa nyata (*real-world*) setelah PC dirakit di lingkungan pengguna biasa. Selain itu, aplikasi pemantau performa yang ada saat ini umumnya hanya menyimpan log secara lokal tanpa fitur komparasi otomatis berbasis spesifikasi yang identik.

**BenchMarkDB** hadir sebagai solusi dengan merekam metrik performa secara terstruktur per judul game, lalu menyimpannya ke database publik agar pengguna dapat membandingkan performa PC mereka secara objektif dengan pengguna lain yang memiliki spesifikasi perangkat keras serupa.

---

## ✨ Fitur Utama
1. **Deteksi Hardware Otomatis:** Memindai spesifikasi komponen utama PC (CPU, GPU, RAM, dan Sistem Operasi) secara otomatis.
2. **Real-Time In-Game Overlay:** Menyediakan *overlay* transparan ringan yang menampilkan FPS saat ini, *Average FPS*, *1% Low FPS*, serta suhu CPU/GPU beserta titik *hotspot*.
3. **Perekaman Telemetri Game:** Mencatat metrik performa dan preset grafis (*Low, Medium, High, Ultra*) secara spesifik per sesi game.
4. **Database Komparasi Publik:** Memungkinkan pencarian dan komparasi data performa berdasarkan kombinasi CPU, GPU, judul game, dan preset grafis yang identik untuk mendeteksi anomali seperti *thermal throttling*.
5. **Manajemen Riwayat & Sinkronisasi Lokal:** Menyimpan riwayat secara lokal jika koneksi terputus dan melakukan pengiriman ulang (*retry*) saat jaringan kembali pulih.

---

## 🛠️ Usulan Arsitektur & Tech Stack
* **Client Side:** Aplikasi Desktop Windows (64-bit) dengan antarmuka berbasis *dark theme* yang ramah bagi *gamer*.
* **Graphics Hooking:** Pustaka penangkapan bingkai untuk API grafis **DirectX 11/12** dan **Vulkan**.
* **Hardware Sensor Reader:** Pustaka pembacaan sensor standar (usulan: *Libre HardwareMonitor* atau API vendor).
* **Backend API:** RESTful API berbasis format JSON melalui protokol aman **HTTPS (TLS 1.2+)**.
* **Database:** DBMS Relasional terindeks performa tinggi (usulan: **PostgreSQL**).

---

## 📂 Struktur Repository
Sesuai dengan ketentuan proyek, struktur direktori dalam repository ini diatur sebagai berikut:

```text
├── Diagram/
│   ├── BPMN As-is dan To-be.png / .svg         
│   ├── User Persona.png / .svg                  
│   └── UML (Use Case, Activity, Class).png / .svg
├── Dokumen/
│   ├── Requirement Traceability Matrix (RTM).pdf / .md                            
│   ├── SRS.pdf / .md         
│   └── Use Case Specification.pdf
└── README.md
