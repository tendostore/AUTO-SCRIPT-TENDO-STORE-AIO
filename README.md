# 🚀 AUTO-SCRIPT-TENDO-STORE-AIO
**EDITION: PLATINUM CLEAN V.6.0 (ULTIMATE FINAL)**

![Version](https://img.shields.io/badge/Version-v01.03.26-blue?style=for-the-badge)
![OS](https://img.shields.io/badge/OS-Ubuntu%20%7C%20Debian-success?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)
![Developer](https://img.shields.io/badge/Developer-Tendo%20Store-orange?style=for-the-badge)

**Auto-Script-Tendo-Store-AIO** adalah *Auto Installer Script* tingkat produksi (Production-Ready) yang dirancang khusus untuk membangun server VPN, SSH, dan tunneling dengan fitur terlengkap dalam satu VPS. Sangat cocok digunakan untuk penjual layanan VPN (Seller SSH), pengelola RT/RW Net, maupun penggunaan pribadi tingkat lanjut. Didesain dengan antarmuka terminal interaktif, fitur keamanan otomatis tingkat dewa, dan integrasi penuh dengan Telegram Bot.

---

## 📑 Daftar Isi
1. [Fitur Unggulan](#-fitur-unggulan)
2. [Informasi Port & Layanan](#-informasi-port--layanan)
3. [Persyaratan Sistem](#-persyaratan-sistem-system-requirements)
4. [Cara Instalasi](#-cara-instalasi-quick-start)
5. [Panduan Setup Bot Telegram](#-panduan-setup-bot-telegram)
6. [Struktur Menu Lengkap](#-struktur-menu-lengkap)
7. [FAQ & Troubleshooting](#-faq--troubleshooting)
8. [Kontak & Dukungan](#-kontak--dukungan)

---

## 🌟 Fitur Unggulan

### 🛡️ 1. Multi-Protocol Terpadu (All-in-One)
- **X-RAY Core V1.8+:** Mendukung protokol VMESS, VLESS, dan TROJAN secara simultan. Mendukung tipe jaringan `WS (WebSocket)`, `gRPC`, dan `HTTPUpgrade` dengan opsi TLS dan Non-TLS.
- **SSH & OpenVPN:** OpenSSH, Dropbear 2019 terbaru, dan Stunnel4 untuk enkripsi SSL/TLS.
- **Robust WS Python Proxy:** Skrip menggunakan proxy Python khusus yang sangat tangguh untuk menangani *payload* WebSocket, meminimalisir masalah *disconnect* atau bengong pada aplikasi seperti HTTP Custom/Netmod.
- **Gaming & Video Call:** Dilengkapi Badvpn / UDPGW untuk kelancaran *gaming* dan *video call* WhatsApp.
- **ZIVPN UDP:** Protokol kustom UDP untuk melakukan *bypass* pada *firewall* ISP tertentu.

### 🤖 2. Otomatisasi & Sistem Keamanan (Cron Jobs)
- **Strict User Validation:** Skrip akan menolak pembuatan akun jika *username* atau ID/Password sudah pernah digunakan.
- **Auto-Kill Expired:** Semua akun (SSH, X-ray, ZIVPN) yang melewati masa aktif akan otomatis dihapus oleh sistem setiap menit.
- **Limit Multi-Login (IP & Session Lock):** Mencegah akun digunakan beramai-ramai. Jika login melebihi batas, akun terkunci otomatis selama 10 menit (*Auto-Lock*), dan akan terbuka kembali secara otomatis (*Auto-Unlock*).
- **Limit Kuota Bandwidth (GB):** Khusus pengguna X-ray, akun otomatis terhapus jika akumulasi *download/upload* menyentuh batas kuota (menggunakan kalkulasi API lokal yang sangat akurat).
- **System Optimizer:** Konfigurasi TCP BBR, fq qdisc, dan Auto-Swap 2GB untuk menjaga performa VPS tetap stabil meski beban tinggi.

### 📱 3. Integrasi Telegram Bot (Real-Time Tracker)
- **Account Creation Receipt:** Notifikasi struk pembuatan akun langsung masuk ke Telegram (lengkap dengan Payload, Expired, dan Limit).
- **Absolute Active Login Tracker:** Bot melacak proses *login* SSH dan X-ray secara 100% akurat. Anda akan menerima laporan jumlah akun yang sedang *online* ke Telegram secara *real-time* (Interval waktu bisa diatur).
- **Auto-Backup & Restore VPS:** Melakukan pencadangan (*Backup*) seluruh *database* VPS (Akun, Kuota, Konfigurasi Bot, Banner) ke dalam file `.zip` dan dikirim langsung ke Telegram. File `.zip` ini bisa di-restore kapan saja dengan sekali klik **tanpa perlu Reboot VPS**.

---

## 🔌 Informasi Port & Layanan

Skrip ini secara otomatis membuka dan mengonfigurasi port berikut pada VPS Anda:

| Layanan | Port Terbuka | Keterangan |
| :--- | :--- | :--- |
| **OpenSSH** | `22`, `444` | Akses SSH standar. |
| **Dropbear** | `90` | Akses SSH ringan. |
| **Stunnel4** | `8443` | SSL/TLS Tunneling (Dropbear TLS). |
| **SSH WS (Proxy)**| `80`, `8080`, `2082`, `2083`, `8880` | None TLS Payload WebSocket. |
| **X-ray TLS** | `443` | Port utama untuk VMESS, VLESS, TROJAN (TLS). |
| **X-ray None TLS** | `80` | Port alternatif VMESS, VLESS, TROJAN (None TLS). |
| **Badvpn UDPGW** | `7100`, `7200`, `7300` | Port UDP untuk Game Online. |
| **ZIVPN UDP** | `5667` | Port khusus protokol ZIVPN. |

---

## ⚙️ Persyaratan Sistem (System Requirements)

Sangat disarankan untuk menggunakan VPS dengan kondisi **OS Fresh Install** untuk menghindari bentrok (*clash*) paket Linux. Mendukung sistem virtualisasi KVM, VMware, dan Cloud (DigitalOcean, Linode, AWS, dll).

- **Sistem Operasi:** - Ubuntu 20.04 LTS / 22.04 LTS
  - Debian 11 / 12
- **Spesifikasi Minimal:** 1GB RAM, 1 Core CPU. (Disarankan RAM 2GB+)
- **Hak Akses:** Akses `root` wajib.

---

## 📥 Cara Instalasi (Quick Start)

Login ke VPS Anda melalui aplikasi terminal (seperti Termius, JuiceSSH, atau PuTTY) menggunakan user `root`. Jalankan baris perintah berikut:

```bash
apt update -y && apt upgrade -y && apt install -y wget curl && wget -q [https://raw.githubusercontent.com/tendostore/AUTO-SCRIPT-TENDO-STORE-AIO/main/setup](https://raw.githubusercontent.com/tendostore/AUTO-SCRIPT-TENDO-STORE-AIO/main/setup) && chmod +x setup && ./setup
```
### 📥 Catatan Saat Instalasi
Saat proses instalasi, Anda akan diminta untuk menentukan konfigurasi domain:

* 🔹 **[1] Domain Random Tendo**
    * Script akan men-generate subdomain gratis secara otomatis yang diarahkan ke IP VPS Anda via Cloudflare API.
* 🔹 **[2] Domain Sendiri**
    * Pastikan domain Anda sudah di-pointing (**A Record**) ke IP VPS Anda di Cloudflare (Status: **DNS Only**).
* ⚡ **Mode Instalasi**
    * Berjalan secara **Force Auto-Yes** (Latar belakang). Anda tidak perlu menekan *Enter* saat instalasi dependensi.
* ⏳ **Visual Proses**
    * Cukup tunggu hingga animasi **Bouncing Scanner** selesai memproses.

---

### 🤖 Panduan Setup Bot Telegram
Ikuti langkah-langkah berikut untuk mengaktifkan fitur notifikasi dan Auto-Backup:

1.  **BotFather:** Buka Telegram dan cari **@BotFather**.
2.  **Dapatkan Token:** Ketik `/newbot`, lalu ikuti instruksinya untuk mendapatkan **Bot Token**.
3.  **Dapatkan Chat ID:** Cari **@userinfobot** atau **@MissRose_bot** untuk mengetahui **Chat ID** Anda.
4.  **Akses VPS:** Buka terminal VPS Anda, ketik `menu`, lalu pilih **[4] BOT TELEGRAM SETUP**.
5.  **Input Data:** Pilih **[1] Change BOT API & CHATID**, lalu masukkan Token dan Chat ID Anda.
6.  **Atur Durasi:** Aktifkan fitur **Notifikasi Login** dan **Backup** sesuai durasi yang diinginkan (contoh: `1h` untuk 1 jam, `10m` untuk 10 menit).

---

### 🗂️ Struktur Menu Lengkap
Ketik `menu` di terminal untuk mengakses fitur-fitur berikut:

* 📂 **[1] SSH ACCOUNT**
    * Create, Delete, Renew, Check Config, dan Trial Account.
    * Fitur **Lock & Unlock** Account secara manual.
* 🛰️ **[2] X-RAY MANAGER**
    * **VMESS / VLESS / TROJAN:** Mendukung fitur Create (dengan Limit IP & Kuota GB), Delete, Renew, Check, Trial, dan Lock/Unlock.
* 🛡️ **[3] ZIVPN UDP**
    * Create, Delete, Renew, Check, dan Trial.
* ⚙️ **[4] BOT TELEGRAM SETUP**
    * Ganti API/ID, Set Notifikasi User Login, dan Set Notifikasi Auto-Backup.
* 🚀 **[5] FEATURES (Utilitas Penting)**
    * **Monitoring:** Check Bandwidth (Vnstat) & Check Services Status.
    * **Pengujian:** Speedtest by Ookla & Check Benchmark VPS.
    * **Sistem:** Restart All Services, Clear Cache RAM, & Set Auto Reboot Server.
    * **Informasi:** Info System (Neofetch) & Change Domain VPS (Auto renew SSL).
    * **Manajemen Data:** Backup & Restore Data VPS (Direct Link) & Rebuild VPS (Auto Install OS).
    * **Kustomisasi:** Change Banner SSH (Kustom teks login).

---

### 🛠️ FAQ & Troubleshooting

> **Q: Mengapa saya tidak bisa konek internet padahal sudah sukses buat akun?**
> **A:** Pastikan status **Xray Core** dan **Dropbear/WS** di menu dalam keadaan **ON** (Hijau). Coba gunakan fitur `[5] FEATURES` -> `Restart All Services`. Pastikan juga *bug* ISP yang Anda gunakan aktif.

> **Q: Bagaimana cara Restore data dari VPS lama ke VPS baru?**
> **A:** Instal script ini di VPS baru. Di VPS lama, pilih menu **Backup Data** untuk mendapatkan *direct link*. Di VPS baru, masuk ke menu **Restore Data** dan masukkan link tersebut. Semua akun akan pindah otomatis.

> **Q: Apakah Limit Multi-Login berjalan Real-time?**
> **A:** Ya. *Cron script* limitasi berjalan setiap menit. Jika terjadi pelanggaran, akun akan dikunci seketika.

---

### 📞 Kontak & Dukungan
Script ini merupakan karya asli yang dikembangkan eksklusif oleh **Tendo Store**.

* 📢 **Telegram:** [@tendo_32](https://t.me/tendo_32)
* 💬 **WhatsApp:** [+6282224460678](https://wa.me/6282224460678)

---

### ⚠️ Peringatan Hukum (Disclaimer)
**Strictly No Spam, DDOS, Carding, Torrenting, or Hacking!** Penulis tidak bertanggung jawab atas segala bentuk penyalahgunaan skrip untuk tindakan ilegal. Gunakan VPS dengan bijak. Dengan menggunakan script ini, Anda setuju dengan ketentuan tersebut.

**Copyright © 2026 Tendo Store. All Rights Reserved.**
