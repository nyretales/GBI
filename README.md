# 📦 Green Box Indonesia - Web Menu & Order

Website statis sederhana namun modern untuk **Green Box Indonesia**, sebuah usaha kuliner yang menyajikan Nasi Kuning, Snack, dan Minuman. Website ini berfungsi sebagai katalog menu digital yang memungkinkan pelanggan memilih pesanan dan mengirimkannya langsung melalui **WhatsApp**.

## ✨ Fitur Utama

* **Desain Responsif:** Tampilan rapi di HP (2 kolom) dan Laptop/PC (4 kolom).
* **Sistem Keranjang Belanja:** Menghitung total harga dan jumlah item secara otomatis tanpa reload halaman (menggunakan JavaScript).
* **Auto-WhatsApp Checkout:** Format pesanan disusun rapi secara otomatis dan dikirim ke nomor WhatsApp admin.
* **Floating UI:** Tombol keranjang belanja yang melayang (sticky) di bagian bawah layar HP agar mudah diakses.
* **Food Card Modern:** Menampilkan foto produk, nama, dan harga dengan tata letak yang bersih.

## 📂 Struktur Folder

Pastikan susunan file di komputer Anda seperti ini agar website berjalan lancar:

```text
/GreenBoxWebsite
│
├── index.html            <-- File utama (Kode Website)
├── README.md             <-- Dokumentasi ini
└── /img                  <-- Folder untuk menyimpan gambar
    ├── Logo.png          <-- Logo utama
    ├── Nasi Kuning Ayam.jpg
    ├── Burger.jpg
    ├── Kopi Aren.jpg
    └── ... (Gambar menu lainnya sesuai nama di HTML)

🚀 Cara Menjalankan
 * Download semua file proyek ini.
 * Pastikan semua gambar sudah dimasukkan ke dalam folder img.
 * Klik dua kali file index.html.
 * Website akan terbuka di browser (Chrome, Edge, Firefox, atau Safari).
⚙️ Cara Mengedit & Kustomisasi
1. Mengganti Nomor WhatsApp Tujuan
Secara default, pesanan dikirim ke 6287867562304. Untuk mengubahnya:
 * Buka index.html menggunakan Notepad atau VS Code.
 * Scroll ke bagian paling bawah, cari kode Script JavaScript.
 * Temukan baris ini:
   // Ganti nomor HP di bawah ini
let nomorHP = "6287867562304";

 * Ganti angkanya dengan nomor baru (gunakan format 628xxx, jangan pakai 08xxx).
2. Menambah Menu Baru
Untuk menambah menu, copy salah satu blok food-card dan paste di bawahnya. Pastikan Anda mengubah:
 * id pada div (harus unik, misal: id="card-baru").
 * Nama file gambar pada tag <img>.
 * Parameter pada tombol fungsi onclick.
Contoh:
<div class="food-card" id="card-baru">
    <img src="img/MenuBaru.jpg" alt="Menu Baru" class="card-img">
    <div class="card-info">
        <div class="card-name">Nama Menu Baru</div>
        <div class="card-price">15K</div>
        <div class="action-area">
            <button class="btn-add" onclick="tambahItem('card-baru', 'Nama Menu Baru', 15000)">+ Tambah</button>
            <div class="qty-control">
                <button class="btn-qty" onclick="kurangItem('card-baru', 'Nama Menu Baru', 15000)">-</button>
                <span class="qty-display">0</span>
                <button class="btn-qty" onclick="tambahItem('card-baru', 'Nama Menu Baru', 15000)">+</button>
            </div>
        </div>
    </div>
</div>

3. Mengganti Gambar
Cukup ganti file di dalam folder img dengan nama yang sama persis, atau ubah nama file di dalam kode HTML src="img/NamaFile.jpg".
 * Rekomendasi Ukuran: 600x600 pixels (persegi).
 * Format: .jpg atau .png.
🛠️ Teknologi yang Digunakan
 * HTML5 (Struktur)
 * CSS3 (Desain & Layout Grid)
 * Vanilla JavaScript (Logika Keranjang & WA API)
 * Google Fonts (Font Poppins)
© 2025 Green Box Indonesia.

