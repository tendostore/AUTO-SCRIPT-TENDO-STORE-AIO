

```markdown
# 🚀 AUTO SCRIPT TENDO STORE ( AIO )
**Premium VPN Auto Installer Script | X-Ray, ZIVPN, SSH & WebSocket**

**Auto Script Tendo Store (AIO)** adalah skrip instalasi VPN server otomatis (All-In-One) grade Premium yang dirancang khusus untuk performa tinggi, stabilitas, dan keamanan tingkat lanjut. Skrip ini sangat ringan, minim *bug*, dan dilengkapi dengan antarmuka (UI) Terminal yang sangat rapi (Center Grid Layout & Open-Border SysInfo).

---

## 📥 Cara Instalasi (Installation Guide)
Login ke terminal VPS Anda menggunakan akses `root`, lalu jalankan baris perintah di bawah ini:

```bash
apt update -y && apt upgrade -y
wget -qO setup [https://raw.githubusercontent.com/tendostore/AUTO-SCRIPT-TENDO-STORE-AIO/main/setup](https://raw.githubusercontent.com/tendostore/AUTO-SCRIPT-TENDO-STORE-AIO/main/setup)
chmod +x setup
./setup

```

*(Catatan: Pastikan VPS Anda dalam keadaan fresh install (baru) sebelum menjalankan skrip ini).*

---

## 🔥 Fitur Unggulan (Premium Features)

### 🔐 Manajemen Protokol & Jaringan Lengkap

* **SSH & WebSocket (WS)**: Mendukung OpenSSH, Dropbear 2019, dan HTTP Custom Proxy.
* **X-Ray Core**: VMESS, VLESS, dan TROJAN. Mendukung jalur protokol mutakhir (WS, GRPC, HTTPUpgrade). Lengkap dengan konfigurasi Fallback port 443 & 80.
* **ZIVPN UDP**: Bypass VPN super cepat menggunakan protokol UDP Custom (Port 5667).
* **BadVPN UDPGW**: Stabilizer koneksi UDP (Port 7100, 7200, 7300) untuk kebutuhan *Voice Call*, *Video Call* WhatsApp, dan Game Online.
* **Robust Daemon WS Proxy (HOTFIX)**: Anti *Zombie-Thread*. Anda bisa bebas *connect* dan *disconnect* dari aplikasi VPN (seperti HTTP Custom) kapanpun tanpa takut tersangkut (*premature connection*) atau harus me-restart service VPS.

### 🤖 Integrasi Telegram Bot (Super Detail & Akurat)

* **Notifikasi Create Account**: Laporan otomatis saat ada akun baru dibuat.
* **Real-Time Login Tracker**: Bot akan melaporkan pengguna aktif setiap menit. Menampilkan info lengkap: **IP Server, Domain, ISP, Total Login Session/IP, dan Pemakaian Kuota (GB)**.
* **Absolute SSH PID Tracker**: Algoritma pelacakan user SSH 100% akurat menggunakan `pgrep -u`. Tidak ada lagi *bug* notifikasi SSH yang gagal terkirim.
* **Notifikasi Auto-Backup**: File backup data VPS (`.zip`) dikirim otomatis langsung ke chat Telegram Anda (mendukung penjadwalan per-menit/jam).

### 🛡️ Sistem Keamanan & Limitasi Otomatis (Anti-Abuse)

* **Auto-Lock Multi Login**: Mengunci (Lock) akun seketika selama 10 Menit jika pengguna melampaui batas Login IP atau Session yang ditentukan. Dilengkapi notif pelanggaran ke Telegram.
* **Auto-Unlock Hukuman**: Membuka kembali akun yang terkunci secara otomatis setelah masa hukuman 10 menit selesai.
* **Limit Kuota Bandwidth (X-Ray API)**: Akun akan dihapus otomatis jika menembus batas pemakaian Kuota GB harian/bulanan (sistem akumulatif cerdas).
* **Auto-Delete Expired**: Menghapus akun secara otomatis tepat saat masa aktif/kadaluwarsa habis.
* **Anti Duplicate Validation**: Mencegah admin membuat akun dengan *Username* atau *UUID/Password* yang sudah terpakai di protokol lain.

### 🛠️ Fitur Sistem & Utilitas Terpadu

* **Smart Backup & Restore**: Mengamankan semua akun, konfigurasi X-Ray/ZIVPN, Bot Telegram, dan Banner SSH. Saat di-Restore di VPS baru, skrip akan **otomatis membuat ulang (Re-create) System User Linux** tanpa perlu *Reboot* VPS!
* **Auto Domain Cloudflare**: Terintegrasi API Cloudflare untuk *generate* random domain langsung pakai, atau gunakan opsi Domain Pribadi (Custom) + Auto SSL.
* **Network Monitoring**: Cek penggunaan Bandwidth (Vnstat) dan uji kecepatan server via Speedtest Ookla Official & Benchmark YABS.
* **Custom HTML Banner**: Fitur ganti *Welcome Banner* SSH / Dropbear dengan format HTML warna-warni secara *Live* langsung dari dalam menu.
* **Neofetch Welcome Message**: Menampilkan spesifikasi *hardware* OS yang cantik saat Anda pertama kali login ke VPS.
* **OS Rebuilder**: Fitur *Rebuild/Reinstall* sistem operasi (Ubuntu/Debian) langsung dari dalam skrip tanpa harus masuk ke panel hosting.

---

## 🌐 Informasi Port Layanan (Port Information)

| Layanan / Protokol | Port yang Digunakan |
| --- | --- |
| **OpenSSH** | `22`, `444` |
| **Dropbear** | `90` |
| **SSH WebSocket (WS)** | `80`, `8080`, `2082`, `2083`, `8880` |
| **SSH WS TLS / SSL** | `443`, `8443` |
| **X-Ray Vmess/Vless/Trojan** | `443` (TLS), `80` (Non-TLS) |
| **ZIVPN (UDP)** | `5667` |
| **Badvpn UDPGW** | `7100`, `7200`, `7300` |

---

## 🖥️ Tampilan Dashboard Utama (Preview)

Dilengkapi dengan antarmuka UI ASCII rata tengah (*Center*) yang *eye-catching*, interaktif, rapi, dan mudah dinavigasi.

```text
┌──────────────────────────────────────────────────────┐
│           AUTO SCRIPT TENDO STORE ( AIO )            │
└──────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────┐
│  OS      : Ubuntu 22.04.5 LTS                        
│  RAM     : 3916MB                                    
│  SWAP    : 2047MB                                    
│  CITY    : Singapore                                 
│  ISP     : AS26277 ServerPoint.com                   
│  IP      : 64.235.41.148                             
│  DOMAIN  : vpn-xray.vip3-tendo.my.id                 
│  UPTIME  : 2 hours, 14 minutes                       
│  ————————————————————————————                        
│  MONTH   : 123.97 MiB    [March]                     
│  RX      : 85.50 MiB                                 
│  TX      : 38.47 MiB                                 
│  ————————————————————————————                        
│  DAY     : 123.97 MiB    [Sunday]                    
│  RX      : 85.50 MiB                                 
│  TX      : 38.47 MiB                                 
│  TRAFFIC : .05 Mbit/s                                
└──────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────┐
│  STATUS  : XRAY: ON | SSH/WS: ON | ZIVPN: ON         │
└──────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────┐
│                      LIST USER                       │
│             ————————————————————————————             │
│   SSH/WS : 2 USR   |   VMESS : 0 USR                 │
│   VLESS  : 0 USR   |   TROJAN: 0 USR                 │
│   ZIVPN  : 0 USR   |   ALL   : 2 USR                 │
└──────────────────────────────────────────────────────┘
        ┌──────────────────────────────────────┐
                Version   :  v01.03.26         
                Owner     :  Tendo Store       
                Telegram  :  @tendo_32         
                Expiry In :  Lifetime          
        └──────────────────────────────────────┘
┌──────────────────────────────────────────────────────┐
│ [1] SSH ACCOUNT          [4] BOT TELEGRAM SETUP      │
│ [2] X-RAY MANAGER        [5] FEATURES                │
│ [3] ZIVPN UDP            [x] EXIT                    │
└──────────────────────────────────────────────────────┘

```

---

## ⚙️ Persyaratan Sistem (System Requirements)

* **OS Supported:** Ubuntu 20.04 / 22.04 LTS & Debian 11 / 12
* **Arsitektur:** x86_64 / amd64
* **Akses:** Wajib `root` (Root Privileges)

---

### 📞 Kontak & Dukungan

Untuk pembaruan skrip, pertanyaan, atau laporan *bug*, silakan hubungi pengembang skrip:

* **Telegram** : [@tendo_32](https://www.google.com/search?q=https://t.me/tendo_32)
* **WhatsApp** : +6282224460678
* **Developer**: Tendo Store

*Strictly No Spam, DDOS, or Hacking.*

```

```
