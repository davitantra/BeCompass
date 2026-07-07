# Spec: Outline Presentasi — Akselerasi Kontrol Aktivitas Kritis (CV + Interlock)

## Konteks

Manajemen mendorong tempo delivery/produksi lebih cepat. Kontrol aktivitas kritis (Ijin Kerja Khusus/IKK) saat ini sebagian besar masih bertumpu pada verifikasi manual (OKK tiap 3 jam, checklist, self-declaration) sebagaimana dianalisis di `docs/references/BeCompass_Referensi_Ijin_Kerja_Khusus_v2.md`. Kontrol manual punya dua gap struktural: rentan "dibohongi" dan tidak scalable seiring tempo naik. Interlock digital/fisik (`docs/references/BeCompass_Metode_Konvensional_vs_Interlock_v3.md`) adalah kontrol paling andal, tapi sebagian item butuh integrasi hardware/PLC/OEM yang mahal & lama. Computer Vision (`docs/references/BeCompass_Computer_Vision_v4.md`) diposisikan sebagai jembatan — lebih cepat & murah di-POC dibanding interlock, lebih objektif dibanding observasi manual — dengan dua tahap kematangan (CV+Alert, lalu CV+Automasi untuk risiko non-fatal/dengan redundansi).

Repo ini juga sudah punya `docs/references/storyline-presentasi-cctv.md` (skeleton presentasi CCTV versi awal, audiens Kepala Teknik Tambang, scope terbatas ke CCTV) beserta `checklist-klarifikasi-vendor-cctv.md` dan `scoring-matrix-vendor-cctv.md` (alat evaluasi vendor CCTV). Spec ini adalah **presentasi baru yang lebih luas**: audiensnya manajemen (bukan Kepala Teknik Tambang), scope-nya mencakup roadmap interlock juga (bukan cuma CCTV/CV), dan tujuannya spesifik meminta blessing engagement vendor + persetujuan budget. Dokumen vendor checklist/scoring existing tetap dipakai sebagai alat kerja di tahap seleksi vendor CV pasca-persetujuan (dirujuk di slide 8 & appendix).

## Tujuan Presentasi

1. Mendapat **blessing** untuk memulai proses seleksi & engagement 3rd party (dua lingkup kerja: vendor CV, vendor/OEM interlock).
2. Mendapat **persetujuan budget** bertahap (Fase 1 POC + alokasi awal Fase 2) untuk menjalankan program ini.

## Audiens & Format

- Audiens: manajemen (bukan level teknis lapangan) — presentasi harus actionable dan sampai ke keputusan dengan cepat.
- Durasi slot: 15-20 menit → 11 slide inti + cover + appendix.
- Framework: **SCR (Situation-Complication-Resolution) + Pyramid Principle (Governing Thought di depan)** — dipilih karena paling padat & actionable untuk audiens yang ingin cepat sampai ke keputusan, dibanding alternatif Three Horizons (butuh lebih banyak slide) atau Problem-Solution-Value sederhana (kurang preventif menjawab keberatan sebelum muncul).
- Level detail: slide-by-slide skeleton — action title (pesan kunci) + bullet pendukung + saran visual per slide, siap dipindah ke PowerPoint.
- Data pendukung (angka insiden, biaya, budget) ditandai `[DATA: ...]` sebagai placeholder — diisi tim sebelum jadi slide final.
- 3rd party dibingkai generik (tanpa nama vendor spesifik di slide) — dua lingkup kerja terpisah yang berpotensi diisi vendor berbeda: vendor CV dan vendor/OEM interlock. Ask ke manajemen adalah blessing untuk *memulai proses seleksi*, bukan approval vendor tertentu.

## Outline Slide

### Slide 1 — Cover
- Judul: "Mempercepat Pengendalian Aktivitas Kritis: Dari Manual ke Machine-Assisted"
- Sub-judul: Program Akselerasi Kontrol BeCompass — Computer Vision & Interlock
- [Ditujukan kepada / tanggal — placeholder]

### Slide 2 — Executive Summary (Governing Thought)
**Action title:** Untuk mengimbangi percepatan delivery bisnis tanpa mengorbankan keselamatan, kami usulkan model kontrol dua-kecepatan — CV sebagai jembatan cepat, interlock sebagai tujuan akhir — yang membutuhkan blessing engagement vendor & persetujuan budget bertahap.

- Tempo operasi meningkat; kontrol kritis saat ini bertumpu pada verifikasi manual yang tidak scalable & rentan gap kepatuhan
- Interlock penuh adalah solusi ideal tapi butuh waktu/biaya integrasi tinggi untuk diterapkan di semua titik sekaligus
- Computer Vision memanfaatkan infrastruktur kamera/drone existing sebagai jembatan cepat & objektif sebelum interlock siap
- Dibutuhkan mitra 3rd party (lingkup CV & lingkup interlock) untuk mempercepat delivery kapabilitas ini
- **Ask:** blessing proses seleksi/engagement vendor + persetujuan budget Fase 1
- *Visual:* ringkasan 3-poin ask dalam bentuk ikon/kotak ringkas

### Slide 3 — Situation
**Action title:** Tempo bisnis mendorong operasi lebih cepat, sementara kontrol aktivitas kritis masih bertumpu pada verifikasi manual.

- [DATA: target akselerasi delivery/produksi tahun ini]
- 7 kategori aktivitas kritis (IKK: ketinggian, dekat/atas air, ruang terbatas, pengangkatan, panas, listrik, luar workshop) dikendalikan lewat kombinasi APD, administratif, dan observasi berkala (OKK tiap 3 jam)
- Semua bergantung pada pengawas melakukan pengecekan fisik berkala — tidak ada kontrol yang berjalan kontinu tanpa kehadiran manusia
- *Visual:* diagram lapisan kontrol saat ini (ikon checklist + pengawas + jam "tiap 3 jam")

### Slide 4 — Complication
**Action title:** Kontrol manual punya dua gap struktural — rentan "dibohongi" dan tidak scalable seiring tempo naik — sementara interlock penuh belum bisa diterapkan di semua titik sekaligus.

- **Gap 1 — Integritas:** checklist/self-declaration bisa ditandatangani tanpa pengecekan sungguh-sungguh (mis. kepatuhan APD, kesesuaian dokumen kerja)
- **Gap 2 — Skalabilitas:** frekuensi observasi manual tetap sama meski volume/tempo aktivitas naik → celah waktu deteksi makin lebar
- Interlock digital/fisik adalah kontrol paling andal (tidak bergantung kejujuran individu), tapi beberapa item butuh integrasi hardware/PLC/OEM yang mahal & lama
- Sebagian item bahkan belum feasible interlock dalam jangka pendek — perlu jembatan
- *Visual:* diagram dua garis yang makin divergen ("tempo operasi" naik vs "frekuensi deteksi manual" tetap datar)

### Slide 5 — Resolution: Model Kontrol Dua-Kecepatan
**Action title:** Kami mengusulkan tangga maturitas kontrol: CV+Alert → CV+Automasi → Interlock, berjalan paralel sesuai tingkat kematangan teknologi & kekritisan risiko.

- **Tahap 1 (CV+Alert):** model mendeteksi kondisi tidak sesuai → notifikasi ke pengawas/CCR → manusia bertindak
- **Tahap 2 (CV+Automasi):** deteksi terhubung ke aksi otomatis — hanya untuk risiko non-fatal, atau risiko fatal dengan redundansi sensor fisik
- **Interlock (fisik/digital penuh):** kontrol akhir untuk risiko fatal yang sama sekali tidak bergantung kejujuran individu
- Tiap aktivitas kritis dipetakan ke tahap yang paling sesuai dengan kematangan teknologi & tingkat fatalitas risikonya — bukan pendekatan satu ukuran untuk semua
- *Visual:* tangga maturitas 3 anak tangga, dengan contoh item risiko ditempatkan di masing-masing tangga

### Slide 6 — Mengapa CV Jadi Jembatan yang Tepat
**Action title:** CV bukan pengganti interlock, tapi jembatan yang lebih cepat, lebih murah, dan lebih objektif dibanding observasi manual.

- **Lebih cepat & murah di-POC:** memakai infrastruktur kamera CCTV/drone yang sudah/akan ada, tidak perlu integrasi ke PLC/OEM alat berat
- **Lebih objektif:** mendekati deteksi kontinu dibanding observasi berkala (OKK tiap 3 jam) yang rentan "dibohongi"
- **Tapi tetap terbatas:** bersifat visual/behavioral — tidak bisa mendeteksi bahaya yang tidak kasat mata (konsentrasi gas, status energized listrik, kegagalan struktur internal) → risiko-risiko itu tetap butuh interlock fisik, bukan CV
- *Visual:* tabel perbandingan 3 kolom (Observasi Manual vs CV vs Interlock) berdasarkan dimensi kecepatan POC, biaya, objektivitas, keandalan untuk risiko fatal

### Slide 7 — Roadmap Prioritas
**Action title:** Prioritas POC dimulai dari use case CV paling matang, berjalan paralel dengan item interlock yang sudah terbukti industri.

- **Quick-win CV (matang, murah):** PPE detection generik, fire/smoke detection, zone intrusion, ANPR gate, drone flyover dokumentasi
- **Interlock prioritas paralel (matang industri):** Electronic LOTO, confined space gas-lock, Load Moment Indicator + Proximity Detection System pada alat angkat
- **Fasing:** Fase 1 (0-3 bulan) POC quick-win CV; Fase 2 (3-6 bulan) scale CV + mulai integrasi interlock prioritas; Fase 3 (6-12 bulan) automasi bertahap untuk use case yang sudah matang
- *Visual:* roadmap timeline dengan 2 swimlane (jalur CV / jalur Interlock) sejajar per fase

### Slide 8 — Mengapa Perlu Mitra 3rd Party
**Action title:** Dua lingkup kerja berbeda dibutuhkan — CV dan Interlock — yang kecepatan & kapabilitasnya belum kami miliki in-house.

- **Vendor CV:** model training & deployment berbasis infrastruktur kamera/drone existing
- **Vendor/OEM Interlock:** integrasi sensor-PLC untuk item prioritas tinggi (LOTO, gas-lock, LMI+PDS)
- In-house belum punya kapabilitas & kecepatan membangun dari nol untuk kedua lingkup ini dalam waktu yang dituntut tempo bisnis
- Engagement paralel (bukan sekuensial) mempercepat time-to-value
- Proses seleksi vendor CV akan memakai kriteria & alat evaluasi yang sudah disiapkan tim (`docs/references/checklist-klarifikasi-vendor-cctv.md`, `docs/references/scoring-matrix-vendor-cctv.md`)
- *Visual:* diagram dua jalur vendor (CV / Interlock) dengan contoh kapabilitas yang dibawa masing-masing

### Slide 9 — The Ask
**Action title:** Kami meminta dua persetujuan: blessing memulai proses seleksi/engagement vendor, dan persetujuan budget bertahap.

- **Ask 1:** Blessing untuk memulai proses seleksi & engagement 2 lingkup vendor (CV & Interlock)
- **Ask 2:** Persetujuan budget Fase 1 (POC, [DATA: indikatif]) + alokasi awal Fase 2
- Keputusan vendor final tetap melalui proses procurement/evaluasi standar (lihat scoring matrix) — ask hari ini adalah blessing untuk *memulai* proses, bukan menyetujui vendor tertentu
- *Visual:* tabel budget indikatif per fase (placeholder angka) + ringkasan 2 ask dalam kotak keputusan

### Slide 10 — Risiko & Mitigasi
**Action title:** Kami sadar CV punya keterbatasan — mitigasi dirancang agar tidak overclaim kapabilitasnya.

- CV tidak bisa mendeteksi bahaya tidak kasat mata (gas, status listrik, kegagalan struktur) → risiko fatal tsb tetap mengandalkan kontrol fisik/interlock, bukan CV
- False negative pada Tahap 1 (CV+Alert) ditanggung sebagai keterbatasan yang diketahui, bukan kegagalan sistem
- Tahap 2 (automasi) hanya dibuka untuk risiko non-fatal, atau risiko fatal dengan redundansi sensor fisik — bukan default
- Governance: kriteria kematangan model + risk assessment menentukan item mana yang boleh naik ke Tahap 2
- *Visual:* tabel 2 kolom risiko vs mitigasi

### Slide 11 — Next Steps & Timeline
**Action title:** Dengan persetujuan hari ini, program dapat mulai berjalan dalam 30 hari.

- **30 hari:** finalisasi kriteria & proses seleksi vendor (2 lingkup)
- **60 hari:** kontrak & kickoff POC quick-win pertama
- **90 hari:** hasil POC awal direview, keputusan scale-up
- *Visual:* timeline bar 30-60-90 hari

### Appendix
- Tabel detail risiko-kontrol per kategori aktivitas kritis (ringkasan dari `BeCompass_Referensi_Ijin_Kerja_Khusus_v2.md`)
- Tabel konvensional vs interlock per risiko (ringkasan dari `BeCompass_Metode_Konvensional_vs_Interlock_v3.md`)
- Tabel use case CV per risiko + tahap kematangan (ringkasan dari `BeCompass_Computer_Vision_v4.md`)
- Ringkasan prioritas POC computer vision (dari `BeCompass_Computer_Vision_v4.md`)
- Breakdown budget detail per fase [placeholder]
- Checklist klarifikasi & scoring matrix vendor CV (rujuk dokumen existing di `docs/references/`)

## Test Kualitas (dari konvensi repo ini)

- **Tes Logika Horizontal:** Judul slide 1→11 dibaca berurutan membentuk satu cerita utuh: ringkasan-ask → situasi → masalah kontrol → solusi dua-kecepatan → alasan CV → roadmap → alasan butuh vendor → ask detail → risiko/mitigasi → next steps.
- **Tes Logika Vertikal:** Tiap bullet pada slide langsung mendukung action title-nya, bukan sekadar topik terkait.
- **Batas slide inti:** 11 slide (di luar cover & appendix) — dalam batas rekomendasi 5-9 pesan utama untuk audiens pengambil keputusan; sedikit lebih banyak karena scope mencakup dua topik (CV dan interlock) sekaligus dua ask (blessing + budget).

## Item Belum Final (perlu diisi sebelum jadi slide PowerPoint)

- Angka target akselerasi delivery/produksi (Slide 3)
- Estimasi budget indikatif per fase (Slide 2, 9, appendix)
- Nama forum/tanggal presentasi (Cover)
