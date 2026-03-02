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
