# 📊 BenchMarkDB (BMDB-V1.0)

> **Aplikasi Monitoring Telemetri & Database Komparasi Performa PC Berbasis Real-World Condition**

Dokumentasi resmi dan repositori proyek untuk mata kuliah **Analisis dan Desain Perangkat Lunak (INF.62.0025)**.

---

## 👥 Identitas Kelompok (Kelompok 3)
* **Bakthi Ananda Harisona** (24343085)[cite: 4, 6]
* **Ganeza Pratama** (24343116)[cite: 4, 6]
* **Muhammad Lintang Azhuri** (24343062)[cite: 4, 6]
* **Dosen Pengampu:** Randi Proska Sandra, S.Pd, M.Sc[cite: 6]
* **Institusi:** Universitas Negeri Padang (Departemen Teknik Elektronika - Teknik Informatika)[cite: 24]

---

## 🚀 Latar Belakang & Problem Framing
Video benchmark yang tersedia di platform seperti YouTube atau forum online umumnya diuji pada kondisi pengujian yang ideal (ruangan ber-AC, komponen kelas atas, *cooler* mahal), sehingga sering kali berbeda dengan performa nyata (*real-world*) setelah PC dirakit di lingkungan pengguna biasa[cite: 16]. Selain itu, aplikasi pemantau performa yang ada saat ini umumnya hanya menyimpan log secara lokal tanpa fitur komparasi otomatis berbasis spesifikasi yang identik[cite: 16].

**BenchMarkDB** hadir sebagai solusi dengan merekam metrik performa secara terstruktur per judul game, lalu menyimpannya ke database publik agar pengguna dapat membandingkan performa PC mereka secara objektif dengan pengguna lain yang memiliki spesifikasi perangkat keras serupa[cite: 16].

---

## ✨ Fitur Utama
1. **Deteksi Hardware Otomatis:** Memindai spesifikasi komponen utama PC (CPU, GPU, RAM, dan Sistem Operasi) secara otomatis[cite: 18].
2. **Real-Time In-Game Overlay:** Menyediakan *overlay* transparan ringan yang menampilkan FPS saat ini, *Average FPS*, *1% Low FPS*, serta suhu CPU/GPU beserta titik *hotspot*[cite: 18].
3. **Perekaman Telemetri Game:** Mencatat metrik performa dan preset grafis (*Low, Medium, High, Ultra*) secara spesifik per sesi game[cite: 18].
4. **Database Komparasi Publik:** Memungkinkan pencarian dan komparasi data performa berdasarkan kombinasi CPU, GPU, judul game, dan preset grafis yang identik untuk mendeteksi anomali seperti *thermal throttling*[cite: 16, 18].
5. **Manajemen Riwayat & Sinkronisasi Lokal:** Menyimpan riwayat secara lokal jika koneksi terputus dan melakukan pengiriman ulang (*retry*) saat jaringan kembali pulih[cite: 21].

---

## 🛠️ Usulan Arsitektur & Tech Stack
* **Client Side:** Aplikasi Desktop Windows (64-bit) dengan antarmuka berbasis *dark theme* yang ramah bagi *gamer*[cite: 20, 21].
* **Graphics Hooking:** Pustaka penangkapan bingkai untuk API grafis **DirectX 11/12** dan **Vulkan**[cite: 20].
* **Hardware Sensor Reader:** Pustaka pembacaan sensor standar (usulan: *Libre HardwareMonitor* atau API vendor)[cite: 20].
* **Backend API:** RESTful API berbasis format JSON melalui protokol aman **HTTPS (TLS 1.2+)**[cite: 20, 21].
* **Database:** DBMS Relasional terindeks performa tinggi (usulan: **PostgreSQL**)[cite: 20].

---

## 📂 Struktur Repository
Sesuai dengan ketentuan proyek, struktur direktori dalam repository ini diatur sebagai berikut[cite: 1]:

```text
├── Diagram/
│   ├── BPMN As-is dan To-be.png / .svg         [cite: 1, 3]
│   ├── User Persona.png / .svg                  [cite: 1, 4]
│   └── UML (Use Case, Activity, Class).png / .svg[cite: 1, 5]
├── Dokumen/
│   ├── SRS.pdf / .md                            [cite: 1, 14]
│   ├── Use Case Specification.pdf / .md         [cite: 1, 24]
│   └── Requirement Traceability Matrix (RTM).pdf[cite: 1, 6]
└── README.md
