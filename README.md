# SIM Logistik — Politeknik Bhakti Kartini

Aplikasi **statis** (HTML + CSS + JavaScript) untuk manajemen logistik kampus: pesan rutin dengan
kuota unit, pesan non-rutin, persetujuan manager, persiapan gudang, katalog & barang masuk,
laporan direktur, dan banner pengumuman. Tampilan mengikuti website Politeknik Bhakti Kartini
(warna biru navy `#0e3a6e` + aksen amber `#f5a623`, font Lora + Plus Jakarta Sans).
Tidak membutuhkan PHP maupun MySQL, sehingga bisa langsung berjalan di **GitHub Pages**.

## Struktur

```
index.html      <- halaman aplikasi
css/style.css   <- tema PBK
js/app.js       <- seluruh logika aplikasi + data demo
images/         <- logo.png dan gambar banner
.nojekyll
```

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (contoh: `sim-logistik-pbk`).
2. Upload **isi folder ini** (bukan folder pembungkusnya) sehingga `index.html` ada di root repository.
3. Buka **Settings → Pages**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu 1–2 menit. Situs tampil di `https://USERNAME.github.io/NAMA-REPO/`.

## Mengubah data

- Data demo (pengguna, unit, katalog, kuota, pesanan) ada di bagian atas `js/app.js`, objek `db`.
- Nama pengguna, jabatan, dan nomor WhatsApp di sana adalah **contoh**; ganti dengan data sebenarnya.
- Logo & banner: ganti file di `images/` (nama file sama) atau ubah lewat menu **Setting Iklan Banner**.

## Catatan penting

- Data **tidak tersimpan permanen**: setiap halaman dimuat ulang, data kembali ke data demo.
  Untuk penyimpanan nyata, perlu backend (mis. Supabase/Firebase) atau fitur localStorage.
- Pilihan peran di sidebar hanya untuk simulasi alur; belum ada login sungguhan.
