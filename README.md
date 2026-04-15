
<p align="center">
  <img src="https://img.shields.io/badge/STUDIOSTAFF%C2%AE-Staff%20Operating%20System-black?style=for-the-badge" alt="STUDIOSTAFF Banner">
</p>

<h1 align="center">House of EXP — Staff OS</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-0078D4?style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/Status-Internal_Use_Only-FF0000?style=flat-square" alt="Status">
  <img src="https://img.shields.io/badge/Deployment-Vercel%20%2B%20Supabase-000000?style=flat-square&logo=vercel" alt="Deployment">
  <img src="https://img.shields.io/badge/Location-Bandung%2C%20ID-brightgreen?style=flat-square" alt="Location">
</p>

---

### 📝 Deskripsi Singkat
**STUDIOSTAFF®** adalah sistem operasi internal House of EXP yang dirancang untuk memusatkan seluruh alur kerja studio musik ke dalam satu dashboard. Mulai dari manajemen proyek, pelacakan klien, keuangan, hingga operasional akademi dan merchandise.

> [!IMPORTANT]
> Sistem ini bersifat **Konfidensial**. Akses hanya diberikan kepada staf resmi House of EXP melalui kredensial yang telah ditentukan.

---

## 🗺️ Navigasi Cepat
- [📖 Ringkasan Umum](#-ringkasan-umum)
- [🖥️ Fitur Utama](#-fitur-utama)
- [💰 Manajemen Keuangan](#-manajemen-keuangan)
- [📦 Produk & Akademi](#-produk--akademi)
- [🚀 Panduan Deployment](#-panduan-deployment)
- [🚦 Referensi Status](#-referensi-status)

---

## 📖 Ringkasan Umum

Sistem berjalan sebagai **Single Page Application (SPA)**. Data dapat disimpan secara lokal di browser atau disinkronkan ke database cloud untuk kolaborasi tim secara real-time.

### 👥 Kredensial Staf
| Nama | Divisi | Akses | Warna |
| :--- | :--- | :--- | :--- |
| **Aldi** | Studio / Produksi | `aldi` | 🔴 Red |
| **Dissa** | Studio / Operasional | `dissa` | 🟣 Purple |
| **Bil** | Finance / Approver | `bil` | 🟢 Green |

**🔑 Password:** `Express` (Dapat diubah melalui Environment Variables).

---

## 🖥️ Fitur Utama

### 1. Proyek Studio & Tugas
Sistem menggunakan logika **Kanban** dan **Task Tracking**.
- 🛠️ **Otomatisasi Progres:** Persentase progres proyek dihitung secara otomatis berdasarkan tugas yang diselesaikan.
- 📋 **Tampilan:** Tabel, Kanban, dan List Tugas khusus per staf.

### 2. Rental & Booking
Manajemen penyewaan alat dan ruang studio dengan sistem durasi fleksibel (6j - 3 Hari).
- ✨ **Auto-Quote:** Kuotasi harga dibuat otomatis saat booking disimpan.

### 3. Jurnal Harian & Komunikasi
Log aktivitas harian untuk transparansi kerja tim.
- 💬 **Interaksi:** Fitur komentar bertingkat dan reaksi emoji (👍 🔥 😂).

---

## 💰 Manajemen Keuangan

Sistem keuangan terintegrasi langsung dengan mutasi bank dan invoice.

| Fungsi | Detail |
| :--- | :--- |
| **Bank Strip** | Monitoring saldo *live* (BCA, Jenius, NAH). |
| **Invoice Builder** | Pembuatan Quotation (#QEXP) & Invoice (#EXP) otomatis. |
| **Payroll** | Penggajian staf dengan sistem persetujuan dua arah. |
| **Debt Tracker** | Pemisahan otomatis antara Piutang (Green) dan Hutang (Red). |

---

## 📦 Produk & Akademi

### 👕 Merchandise
Manajemen inventaris untuk brand **EXP** dan **NAH**.
- **SKU Builder:** Penamaan otomatis (Contoh: `EXP-AP-001`).
- **Stock Logic:** Pengurangan stok otomatis setiap ada transaksi di *Sales Log*.

### 🎓 Akademi
Sistem manajemen siswa dan kelas musik.
- **Batch Invoicing:** Penagihan iuran kelas ke banyak siswa sekaligus dalam satu klik.
- **Student Portal:** Pelacakan data kehadiran dan status pembayaran siswa.

---

## 🚀 Panduan Deployment

Sistem menggunakan stack **Vercel** untuk hosting dan **Supabase** untuk database.

### Konfigurasi Environment Variables
```env
SUPABASE_URL="https://your-project.supabase.co"
SUPABASE_SERVICE_KEY="your-service-role-key"
STUDIOSTAFF_PASSWORD="YourSecretPassword"
Langkah Cepat Deployment

Jalankan npm install di folder studiostaff-deploy.

Lakukan sinkronisasi schema melalui supabase_schema.sql.

Jalankan vercel --prod untuk merilis aplikasi ke cloud.

🚦 Referensi Status
Badge	Status	Deskripsi

![alt text](https://img.shields.io/badge/Status-Awaiting_Approval-amber)
	Pending	Menunggu persetujuan rekan tim/admin.

![alt text](https://img.shields.io/badge/Status-Approved-green)
	Disetujui	Dokumen/izin telah divalidasi.

![alt text](https://img.shields.io/badge/Status-Paid-blue)
	Lunas	Pembayaran telah diterima dan masuk ke kas.

![alt text](https://img.shields.io/badge/Status-Canceled-red)
	Batal	Proyek atau pesanan dibatalkan.
📞 Kontak Studio

📍 Alamat: Kyomi Space, Jl. Ir. H. Juanda No.130, Dago, Bandung.

📞 WA: +62-812-147-159-13

📧 Email: sonicdesignexp@gmail.com

💳 Billing: BCA 1394227369 (a.n. Islam Bilhaqy)

```

