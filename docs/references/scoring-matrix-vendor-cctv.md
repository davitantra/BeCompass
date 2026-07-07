# Scoring Matrix Evaluasi Vendor CCTV Analitik
### Kriteria Teknis & Non-Teknis

---

## A. Kriteria Teknis
*Mengukur kemampuan sistem vendor memenuhi kebutuhan use case & skema penempatan.*

| Kategori | Bobot | Sumber Pertanyaan |
|---|---|---|
| A1. Kapabilitas Analitik & Sistem | 25% | Bagian 1 — Kapabilitas Teknis |
| A2. Implementasi & Instalasi | 15% | Bagian 2 — Implementasi & Instalasi |
| A3. Keamanan Data & Arsitektur | 10% | Bagian 5 — Keamanan Data & Kepatuhan |
| A4. Exit Strategy / Ketergantungan Sistem | 5% | Bagian 7 — Exit Strategy |
| **Total Bobot Teknis** | **55%** | |

---

## B. Kriteria Non-Teknis
*Mengukur kelayakan & keamanan bermitra dengan vendor tersebut.*

| Kategori | Bobot | Sumber Pertanyaan |
|---|---|---|
| B1. Layanan & Dukungan Pasca-Implementasi | 15% | Bagian 3 — Layanan & Dukungan |
| B2. Komersial | 20% | Bagian 4 — Komersial |
| B3. Legalitas & Kapasitas Perusahaan | 10% | Bagian 6 — Legalitas & Kapasitas Perusahaan |
| **Total Bobot Non-Teknis** | **45%** | |

> Catatan: Total bobot Teknis + Non-Teknis = 100%. Bobot di atas bisa disesuaikan — misalnya jika prioritas utama adalah keselamatan (akurasi deteksi), naikkan bobot A1; jika kekhawatiran utama adalah kontinuitas vendor, naikkan bobot B3.

---

## C. Skala Skor

Setiap pertanyaan pada checklist klarifikasi diberi skor 1–5 berdasarkan jawaban vendor saat meeting:

| Skor | Arti |
|---|---|
| 5 | Sangat memenuhi, ada bukti konkret (data, referensi, demo) |
| 4 | Memenuhi, penjelasan meyakinkan tapi tanpa bukti kuat |
| 3 | Cukup, ada gap kecil atau butuh klarifikasi lanjutan |
| 2 | Kurang memenuhi, ada gap signifikan |
| 1 | Tidak memenuhi / red flag |

---

## D. Cara Menghitung

**Langkah 1 — Skor per Kategori**
```
Skor Kategori = rata-rata skor semua pertanyaan dalam kategori tersebut
```
Contoh: Kategori A1 punya 5 pertanyaan dengan skor 4, 5, 4, 3, 4 → Skor A1 = (4+5+4+3+4) / 5 = 4,0

**Langkah 2 — Skor Total per Vendor**
```
Skor Total = Σ (Skor Kategori × Bobot Kategori)
```
Contoh:
```
Skor Total = (Skor A1 × 25%) + (Skor A2 × 15%) + (Skor A3 × 10%) + (Skor A4 × 5%)
           + (Skor B1 × 15%) + (Skor B2 × 20%) + (Skor B3 × 10%)
```

**Langkah 3 — Skor Teknis vs Non-Teknis (untuk perbandingan cepat)**
```
Skor Teknis     = (Skor A1×25% + Skor A2×15% + Skor A3×10% + Skor A4×5%) / 55%
Skor Non-Teknis = (Skor B1×15% + Skor B2×20% + Skor B3×10%) / 45%
```

---

## E. Kriteria Gugur (Disqualifying Criteria)

Vendor otomatis **gugur**, berapa pun skor totalnya, jika salah satu terjadi:
- Legalitas usaha tidak lengkap atau tidak valid
- Kondisi finansial sangat meragukan (indikasi berisiko bangkrut/berhenti operasi)
- Menolak memberikan kepemilikan data sepenuhnya ke perusahaan
- Tidak bersedia memberikan SLA tertulis untuk penanganan kerusakan

---

## F. Template Tabel Perbandingan Akhir

| Vendor | Skor Teknis (55%) | Skor Non-Teknis (45%) | Skor Total | Kriteria Gugur? | Status |
|---|---|---|---|---|---|
| A | | | | | |
| B | | | | | |
| C | | | | | |

---

## G. Lembar Kerja Skor per Vendor

### Vendor: _______________________

| Kategori | Bobot | Skor (1-5) | Kontribusi (Skor × Bobot) |
|---|---|---|---|
| A1. Kapabilitas Analitik & Sistem | 25% | | |
| A2. Implementasi & Instalasi | 15% | | |
| A3. Keamanan Data & Arsitektur | 10% | | |
| A4. Exit Strategy / Ketergantungan | 5% | | |
| B1. Layanan & Dukungan | 15% | | |
| B2. Komersial | 20% | | |
| B3. Legalitas & Kapasitas Perusahaan | 10% | | |
| **Skor Total** | **100%** | | |

**Kriteria Gugur terpenuhi?** ☐ Ya ☐ Tidak
**Status Akhir:** ☐ Direkomendasikan ☐ Cadangan ☐ Gugur
