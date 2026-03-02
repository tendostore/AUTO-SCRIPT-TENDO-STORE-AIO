# 🚀 Auto Script Install X-RAY, ZIVPN & SSH WS (AIO Premium Edition)

![Release](https://img.shields.io/badge/RELEASE-v01.03.26-3d4451?style=for-the-badge&logo=rocket&labelColor=282c34) ![OS](https://img.shields.io/badge/SUPPORTED-UBUNTU%20%7C%20DEBIAN-e95420?style=for-the-badge&logo=linux&labelColor=282c34) ![Code](https://img.shields.io/badge/CODE-BASH-4eaa25?style=for-the-badge&logo=gnu-bash&labelColor=282c34)

Script Auto Installer All-In-One (AIO) khusus untuk **X-Ray Core, ZIVPN, dan SSH/WS**. Didesain dengan performa tinggi, stabilitas tingkat lanjut, dan memiliki tampilan **Platinum Clean UI** (Center Grid Layout & Neofetch OS Info). Sangat cocok untuk mengelola server VPN Premium dengan sistem otomatisasi keamanan yang ketat.

---

## 📥 PERINTAH INSTALL (INSTALLATION)

Salin dan jalankan perintah di bawah ini pada terminal VPS Anda (Wajib run sebagai root):

```bash
apt update -y && apt upgrade -y && wget -qO setup [https://raw.githubusercontent.com/tendostore/AUTO-SCRIPT-TENDO-STORE-AIO/main/setup](https://raw.githubusercontent.com/tendostore/AUTO-SCRIPT-TENDO-STORE-AIO/main/setup) && chmod +x setup && ./setup

Pastikan VPS dalam keadaan fresh (baru diinstall ulang) untuk hasil terbaik.
⭐ KEUNGGULAN UTAMA (KEY FEATURES)
Script ini difokuskan pada stabilitas jaringan, keamanan anti-abuse, dan kemudahan manajemen:
⚡ 1. Manajemen Protokol & Jaringan Lengkap
 * Mendukung protokol komplit: SSH, WebSocket (WS), OpenSSH, Dropbear 2019, dan HTTP Custom Proxy.
 * Integrasi X-Ray Core (VMESS, VLESS, TROJAN) dengan dukungan jaringan mutakhir (WS, GRPC, HTTPUpgrade).
 * Terintegrasi ZIVPN UDP (Bypass super cepat) dan BadVPN UDPGW (Support Game Online & Voice/Video Call WhatsApp).
 * Memiliki Robust Daemon WS Proxy: Bebas connect/disconnect HTTP Custom kapanpun tanpa stuck (nyangkut) atau perlu restart service.
🤖 2. Integrasi Telegram Bot (Super Detail & Akurat)
 * Real-Time Login Tracker: Melaporkan User aktif tiap menit dengan detail IP Client, Domain, ISP, Total Login Session, dan Sisa Kuota (GB).
 * Absolute SSH PID Tracker: Algoritma pelacakan user SSH 100% akurat menggunakan sistem Process ID (pgrep).
 * Auto Backup Notif: File backup data VPS (.zip) dikirim otomatis langsung ke chat Telegram Anda.
🛡️ 3. Sistem Proteksi Otomatis (Anti-Abuse)
 * Auto-Lock Multi Login: Mengunci akun secara otomatis (Hukuman 10 Menit) jika melanggar batas Login IP/Session.
 * Auto-Unlock Hukuman: Membuka kembali akun yang terkunci setelah masa hukuman selesai.
 * Limit Kuota Bandwidth: Menghapus akun otomatis jika menembus batas pemakaian Kuota (GB).
 * Anti Duplicate Validation: Mencegah admin membuat akun dengan Username/UUID yang bentrok dengan protokol lain.
💎 4. Platinum Clean UI Dashboard
 * Welcome Screen: Otomatis menampilkan spesifikasi OS (neofetch) saat pertama kali login ke VPS.
 * Center Grid Layout: Tampilan menu dan daftar LIST USER (SSH | VMESS | VLESS dll) tersusun rapi presisi di tengah layar dengan gaya Open-Right Border SysInfo.
🛠️ DAFTAR FITUR LENGKAP
📡 Protocols
| Protocol | Transport | Port |
|---|---|---|
| OpenSSH | TCP | 22, 444 |
| Dropbear | TCP | 90 |
| SSH WS | HTTP Proxy | 80, 8080, 2082, 2083, 8880 |
| SSH WS SSL | HTTPS Proxy | 443, 8443 |
| VMess / VLess | WS / GRPC / UPG | 443 (TLS) / 80 (Non-TLS) |
| Trojan | WS / GRPC / UPG | 443 (TLS) |
| ZIVPN | UDP Tunnel | 5667 |
| BadVPN | UDPGW | 7100, 7200, 7300 |
⚙️ Tools & Manager
 * ✅ Create, Delete, Renew, Trial, Lock/Unlock User Account
 * ✅ Smart Backup & Restore (Otomatis Re-create System User Linux tanpa perlu Reboot VPS)
 * ✅ Auto Domain Cloudflare (Random/Custom) + Auto SSL
 * ✅ Live Edit Welcome Banner SSH (HTML)
 * ✅ Speedtest by Ookla & Benchmark VPS (YABS)
 * ✅ Auto Reboot Manager (Scheduler)
 * ✅ OS Rebuilder (Install ulang OS VPS langsung dari dalam script)
 * ✅ Clear RAM Cache & Restart All Services
📞 Hubungi Kami (Contact & Support)
Untuk pembelian script premium, pembaruan, atau bantuan troubleshooting, silakan hubungi pengembang skrip:
 * Telegram : @tendo_32
 * WhatsApp : +6282224460678
 * Developer: Tendo Store
Strictly No Spam, DDOS, or Hacking. Use responsibly.

