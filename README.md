# invitation.me

Sebuah *template* undangan pernikahan digital statis (*Single-Page*) yang mengusung konsep desain **Clean, Minimalist, dan Utilitarian**. Terinspirasi dari antarmuka *dashboard* modern, undangan ini dirancang untuk memuat informasi dengan sangat cepat, ringan, dan langsung pada intinya.

Dibuat sepenuhnya tanpa *backend* atau *database*, memanfaatkan *Vanilla JavaScript* untuk menangani logika personalisasi nama tamu undangan.

## ✨ Fitur Utama

- **Personal Greeting via URL Parameter:** Menyapa nama tamu secara otomatis hanya dengan menambahkan `?to=Nama+Tamu` pada tautan (tanpa perlu *database*).
- **Interactive Cover:** Sampul depan yang mengunci layar (*no-scroll*) hingga tamu menekan tombol "Buka Undangan" dengan animasi *slide-up*.
- **Live Countdown:** Fitur hitung mundur waktu otomatis menuju hari acara (Akad/Resepsi).
- **Grid Gallery:** Susunan galeri foto minimalis yang memuat 10 slot (5 baris, 2 kolom) bergaya *feed*.
- **Digital Gift (Tanda Kasih):** Tombol salin nomor rekening *one-click* (mendukung API navigator.clipboard).
- **Responsive & Mobile-First:** Tampilan yang dioptimalkan 100% untuk layar *smartphone*.

## 🛠️ Tech Stack

- **HTML5** (Semantik)
- **Tailwind CSS** (via CDN untuk *styling* instan)
- **Vanilla JavaScript** (ES6)
- **Google Fonts:** Figtree (Teks Utama) & Great Vibes (Teks Sambung)

## 🚀 Cara Penggunaan

Karena proyek ini bersifat statis (hanya 1 file HTML), Anda tidak perlu melakukan proses *build* atau instalasi npm.

1. Clone repository ini:
```
   git clone https://github.com/HomePrint-Developer/invitation.me.git
   ```

2. Buka file `index.html` langsung di *browser* Anda.

3. Untuk melihat fitur sapaan nama tamu, tambahkan parameter `?to=` di akhir URL.
   Contoh (Localhost):
   file:///.../invitation.me/index.html?to=Bapak%20Budi%20Santoso

## ⚙️ Kustomisasi (Untuk Pengembang)

Anda dapat dengan mudah mengubah data *dummy* menjadi data asli Anda langsung di dalam file `index.html`:

- **Mengatur Countdown Waktu:**
  Cari baris kode JavaScript di bagian paling bawah dan sesuaikan fungsi new Date():
  // Format: Tahun, Bulan (0-11, jadi 6 = Juli), Tanggal, Jam, Menit, Detik
  const targetDate = new Date(2023, 6, 15, 11, 0, 0).getTime(); 

- **Mengganti Foto:**
  Cari tag img dan ganti URL https://via.placeholder.com/... dengan path gambar lokal atau *cloud storage* Anda.

- **Mengubah Bank & Rekening:**
  Cari elemen dengan ID #rek-bri atau tag fungsi salinTeks('rek-bri') dan sesuaikan dengan rekening Anda.

## 🌐 Deployment

Proyek ini sangat ideal untuk di-*deploy* secara gratis menggunakan layanan *static hosting* seperti:
- **GitHub Pages** (Rekomendasi)
- **Netlify**
- **Vercel**

Cukup arahkan *root directory* ke *branch main*, dan web undangan siap disebarkan.

---

**© 2026 Crafted by [M. Aini](https://github.com/HomePrint-Developer)**  
*Anak Teknik Informatika / Sang Ahli Prompt AI*