# Toolkit BPS

Perangkat kerja digital **gratis** untuk satuan kerja Badan Pusat Statistik (BPS).
Dibuat oleh pegawai BPS, untuk BPS — non-profit.

Situs: **https://www.toolkitbps.my.id**

## Aplikasi

| Aplikasi | Tautan | Dikelola di |
|---|---|---|
| Monitoring Pencacahan SE2026 | `monitoring-se.toolkitbps.my.id` + `mse-<daerah>` | VPS (via Cloudflare) |
| Sistem Laporan Kegiatan | `laporan.toolkitbps.my.id` | VPS (via Cloudflare) |
| Dashboard Wilayah Kerja | `wilker.toolkitbps.my.id` | Vercel |
| Pantau Pegawai | `pawai.toolkitbps.my.id` | Vercel |

### Satuan kerja pemakai Monitoring SE2026

| Satuan kerja | Subdomain | Cakupan |
|---|---|---|
| BPS Kabupaten Minahasa Selatan | `monitoring-se` | Kabupaten |
| BPS Provinsi Sulawesi Utara | `mse-sulut` | Provinsi |
| BPS Kabupaten Minahasa | `mse-minahasa` | Kabupaten |
| BPS Kabupaten Minahasa Utara | `mse-minut` | Kabupaten |
| BPS Kota Tomohon | `mse-tomohon` | Kota |
| BPS Kota Manado | `mse-manado` | Kota |

## Struktur repositori

```
index.html            Halaman utama (satu-satunya halaman publik)
favicon.svg           Ikon situs
robots.txt            Aturan perayapan
sitemap.xml           Peta situs
```

## Deployment

Repo ini di-deploy otomatis oleh **Vercel** dari branch `master`.
Push ke `master` → Vercel langsung menerbitkan versi baru (sekitar 1 menit).

Catatan: domain apex `toolkitbps.my.id` melakukan redirect 307 ke
`www.toolkitbps.my.id`, sehingga `canonical` dan `og:url` di `index.html`
diarahkan ke versi `www`.

## Menambah aplikasi baru ke halaman utama

1. Buka `index.html`, cari bagian `<!-- APLIKASI -->`.
2. Duplikasi salah satu blok `<a class="card-hover ...">` yang sudah ada.
3. Ubah judul, deskripsi, tautan, dan warna gradien kartu.
4. Bila aplikasi baru sudah dipakai lebih dari satu satuan kerja, tambahkan
   juga barisnya pada tabel di bagian `<!-- MONITORING SE -->`.
5. Perbarui angka pada bagian `<!-- STATISTIK NYATA -->` bila berubah.

## Kontak

- Email: `admin@toolkitbps.my.id`
- WhatsApp: https://wa.me/6282360054904
