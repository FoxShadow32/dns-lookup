# dns-lookup
🌐 DNS Lookup - Cek IP address dari suatu domain (simple, cepat, tanpa ribet)

# 🌐 DNS Lookup

**DNS Lookup** adalah tools sederhana berbasis Python untuk mencari alamat IP dari suatu domain. Tools ini menggunakan library `socket` bawaan Python, sehingga ringan, cepat, dan tidak memerlukan instalasi dependensi tambahan.

Tools ini cocok untuk:
- 🔍 **OSINT sederhana** – mencari tahu IP address di balik sebuah domain
- 🛠️ **Pembantu scanning** – dapatkan IP target sebelum menggunakan port scanner atau tools lainnya
- 📚 **Belajar DNS** – memahami hubungan antara domain dan IP address

## 🔧 Fitur

| Fitur | Keterangan |
| :--- | :--- |
| **Cek IP domain** | Mengembalikan alamat IPv4 dari domain yang dimasukkan |
| **Input manual** | Bisa dijalankan interaktif dengan mengetik domain saat program berjalan |
| **Argumen langsung** | Bisa langsung kasih domain dari command line |
| **Error handling** | Memberi tahu jika domain tidak ditemukan atau tidak valid |
| **Ringan & cepat** | Tanpa dependensi tambahan, hanya library standar Python |

## 📝 Penggunaan

### Cara 1: Langsung kasih argumen

```bash
python dns_lookup.py google.com

Cara 2: Input manual (program akan meminta domain)
bash
python dns_lookup.py

📊 Contoh Output
$ python dns_lookup.py google.com
╔══════════════════════════════════════════╗
║        🌐 DNS LOOKUP v1.0                ║
║     Cek IP address dari suatu domain     ║
╚══════════════════════════════════════════╝

[+] Mencari IP untuk google.com...

✅ Ditemukan!
   Domain: google.com
   IP    : 142.250.184.46

Jika domain tidak ditemukan:

bash
$ python dns_lookup.py domain_gak_ada.com
text
❌ Gagal! Domain domain_gak_ada.com tidak ditemukan.

📦 Instalasi
git clone https://github.com/FoxShadow32/dns-lookup.git
cd dns-lookup
python dns_lookup.py

Tools ini hanya menggunakan library standar Python, tidak perlu install dependensi tambahan.

📂 Struktur Proyek
dns-lookup/
├── dns_lookup.py    # File utama
├── README.md        # Dokumentasi
├── LICENSE          # MIT License
└── .gitignore       # Abaikan file sampah

🧠 Teknis: Bagaimana Tools Ini Bekerja
Langkah	Penjelasan
1. Baca input	Menerima domain dari argumen atau input manual
2. Resolve domain	Menggunakan socket.gethostbyname() untuk mendapatkan IP
3. Tampilkan hasil	Jika berhasil, tampilkan domain dan IP; jika gagal, beri pesan error

🔗 Terintegrasi dengan Tools Lain
Tools ini bisa dikombinasikan dengan tools lain yang sudah lo buat:

ip-info-lookup – setelah dapet IP, lo bisa cek detail lokasi dan ISP

port-scanner – setelah dapet IP, lo bisa scan port terbuka

📜 Lisensi
Proyek ini dilisensikan di bawah MIT License — bebas digunakan, dimodifikasi, dan didistribusikan.

👤 Penulis
FoxShadow32

GitHub: github.com/FoxShadow32







