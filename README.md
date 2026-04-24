# Hatta Wardhana — Special Concert
### War Tiket · 30 April 2026

Website war pemesanan tiket eksklusif dengan countdown, form nama, dan e-tiket otomatis.

---

## 🚀 Deploy ke Vercel (2 cara)

### Cara 1 — Via Vercel CLI (Recommended)

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Masuk ke folder project
cd hatta-wardhana-concert

# 3. Login ke akun Vercel
vercel login

# 4. Deploy
vercel

# 5. Deploy ke production
vercel --prod
```

### Cara 2 — Via GitHub + Vercel Dashboard

```
1. Push ke GitHub:
   git init
   git add .
   git commit -m "feat: hatta wardhana concert war tiket"
   git branch -M main
   git remote add origin https://github.com/USERNAME/hatta-wardhana-concert.git
   git push -u origin main

2. Buka https://vercel.com/new
3. Klik "Import Git Repository"
4. Pilih repo hatta-wardhana-concert
5. Klik Deploy — selesai!
```

---

## 📁 Struktur File

```
hatta-wardhana-concert/
├── index.html       ← Halaman utama (semua dalam 1 file)
├── vercel.json      ← Konfigurasi Vercel
└── README.md        ← Panduan ini
```

---

## ✏️ Kustomisasi

Edit bagian berikut di `index.html`:

| Baris | Yang diubah |
|-------|-------------|
| `const DEMO_SEC = 20;` | Durasi countdown demo (detik) |
| `30 April 2026` | Tanggal konser |
| `Main Hall Bea Cukai Pasuruan` | Lokasi |
| `Pintu Dibuka Pukul 12.00 WIB` | Jam buka pintu |

### Mengubah ke Countdown Tanggal Nyata

Ganti baris ini di `<script>`:

```js
// SEBELUM (demo 20 detik):
const DEMO_SEC = 20;
const endTime = Date.now() + DEMO_SEC * 1000;
const totalMs = DEMO_SEC * 1000;

// SESUDAH (tanggal nyata, misal 30 April 2026 pukul 09.00 WIB):
const endTime = new Date('2026-04-30T09:00:00+07:00').getTime();
const totalMs = endTime - /* tanggal_launch_website */ new Date('2026-04-01T00:00:00+07:00').getTime();
```

---

## 🌐 Custom Domain di Vercel

1. Buka dashboard project di vercel.com
2. Settings → Domains
3. Tambahkan domain Anda (misal: `tiket.hattawardhana.com`)
4. Arahkan DNS ke Vercel sesuai instruksi

---

Made with ♥ for Hatta Wardhana Special Concert
