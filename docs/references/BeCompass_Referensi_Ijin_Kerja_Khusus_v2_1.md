# Referensi BeCompass — Analisis Risiko & Pengendalian Ijin Kerja Khusus

> Sumber: P-CMP-19 (Prosedur Ijin Kerja Khusus, Rev. 0, 18 Des 2024), S-CMP-19.01 (Standar Ijin Kerja Khusus, Rev. 0), S-CMP-19.02 (Standar Observasi Kerja Khusus, Rev. 0) — PT Berau Coal
>
> Struktur per aktivitas kritis: **Risiko** (bahaya yang sebenarnya ingin dicegah) → **Jenis Pengendalian** (hierarki: Eliminasi/Substitusi/Rekayasa/Administratif/APD) → **Pengendalian yang Dilakukan** (kontrol aktual sesuai dokumen) → **Risiko Sisa** (residual risk yang tetap ada meski kontrol diterapkan) → **Referensi Sumber**.
>
> **Legenda Jenis Pengendalian:** E = Eliminasi | S = Substitusi | R = Rekayasa (Engineering Control) | A = Administratif | APD = Alat Pelindung Diri
>
> Catatan metodologi: (1) Klasifikasi hierarki pengendalian merupakan interpretasi analitis berdasarkan sifat kontrol yang disebutkan dalam dokumen — dokumen sumber sendiri tidak secara eksplisit melabeli hierarki ini. (2) Asosiasi APD/Peralatan ke tiap aktivitas pada S-CMP-19.01 disusun berdasarkan deskripsi item, karena checklist tabel matriks asli kehilangan tanda centang saat ekstraksi teks — disarankan cross-check visual ke PDF asli untuk validasi presisi 100%.

---

## Ketentuan Umum Lintas Aktivitas Kritis

**Aktivitas:** Berlaku untuk seluruh jenis Ijin Kerja Khusus (IKK) sebagai lapisan kontrol dasar sebelum kontrol spesifik per jenis pekerjaan.

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| U1 | Pekerja tidak terdaftar/tidak dikenal ikut bekerja dalam aktivitas berisiko tinggi tanpa terverifikasi kompetensinya | A | List personil terdaftar wajib diverifikasi; kompetensi mengacu S-HCT-04; STOP otomatis bila ada personil tidak terdaftar | Penggantian personil diam-diam di tengah shift tanpa re-verifikasi | P-CMP-19 hal.2 ("Perlu diingat"); §3.6; S-CMP-19.02 hal.1 baris 1 |
| U2 | Pekerjaan dimulai meski kondisi pekerja/APD/dokumen/lingkungan belum layak | A | Inspeksi Pra Kerja (IPK) oleh Pengawas Langsung — 5 parameter wajib sesuai sebelum aktivasi ijin (Check-In) | Penilaian kelayakan bersifat subjektif terhadap pengawas yang melakukan IPK | P-CMP-19 §4.2.1 No.1; hal.2 ("Perlu diingat" poin Layer 1) |
| U3 | Paparan langsung terhadap bahaya spesifik pekerjaan karena APD tidak dipakai dengan benar | APD | APD wajib sesuai Matriks APD per jenis IKK (S-CMP-19.01); STOP otomatis bila tidak sesuai | Kepatuhan pemakaian & kondisi APD (aus/rusak) tetap bergantung perilaku individu | S-CMP-19.02 hal.1 baris 3 |
| U4 | Kegagalan alat kerja saat digunakan (jatuh, terjepit, rusak mendadak) | R + A | Kriteria kelayakan peralatan per jenis (S-CMP-19.01 bag. 2–3) + pemeriksaan P2H sebelum digunakan; STOP otomatis bila tidak sesuai | Cacat tersembunyi pada alat yang tidak terdeteksi inspeksi visual rutin | S-CMP-19.02 hal.1 baris 4 |
| U5 | Bahaya di lapangan menyimpang dari yang teridentifikasi dalam dokumen (JSA/IK tidak representatif) | A | Dokumen kerja (JSA/IK) wajib sesuai lokasi & aktivitas aktual; STOP otomatis bila tidak sesuai | Perubahan kondisi lapangan mendadak setelah dokumen disetujui | S-CMP-19.02 hal.1 baris 5 |
| U6 | Hilangnya kontrol berjenjang karena pengawas tidak menjalankan kewajiban (IPK, observasi 3-jam, closing) | A | Sistem sanksi bertingkat pengawas: Coaching Kabag → Coaching PJO → Suspend KPO Safety 1–3 bulan (lihat tabel Performance Pengawas di bagian akhir) | Sifat kontrol reaktif — sanksi baru berjalan setelah temuan/ketidaksesuaian terjadi, bukan mencegah kejadian pertama | S-CMP-19.01 hal.7 (Performance Pengawas); P-CMP-19 §4.2.1 No.2 |

---

## 1. Kerja di Ketinggian (IKDK)

**Aktivitas:** Pekerjaan pada lokasi >1,8 m dari lantai kerja utama, dengan lantai kerja statis tanpa pagar pengaman (permanen/tidak permanen) tinggi minimal 90 cm. *(P-CMP-19 §3.11)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 1.1 | **Jatuh dari ketinggian** akibat lantai kerja tanpa pagar pengaman | R + APD | Titik kait/life line horizontal sejajar pinggang untuk kerja >10 m; Full Body Harness Double Lanyard dikaitkan pada anchor point yang kuat | Jatuh tetap dapat terjadi bila anchor point/hook tidak dikaitkan dengan benar (faktor manusia) | P-CMP-19 §3.11, §4.4.2.1 poin 9c; S-CMP-19.01 hal.5 No.2; S-CMP-19.02 hal.1 baris 7–8 |
| 1.2 | Jatuh/tergelincir akibat **cuaca buruk** (gerimis, hujan, angin kencang) | A | Larangan mutlak kerja ketinggian saat gerimis/hujan/angin kencang; STOP otomatis pada kondisi lingkungan tidak memenuhi | Perubahan cuaca mendadak selama pekerjaan berlangsung sebelum sempat dihentikan | P-CMP-19 §4.4.2.1 poin 3; S-CMP-19.02 hal.1 baris 6 |
| 1.3 | **Keruntuhan perancah** (scaffolding) yang menyebabkan pekerja jatuh bersama struktur | R + A | Perancah dibuat teknisi tersertifikasi & diperiksa supervisor tersertifikasi; assessment inspektor scaffolding sebelum kerja; Scaffold Tag Hijau harian; penghentian kerja saat ada perubahan lift/kolom untuk pemeriksaan ulang | Kegagalan komponen tersembunyi (korosi internal, cacat material) tidak selalu terdeteksi inspeksi visual | P-CMP-19 §4.4.2.1 poin 4, 7–8; S-CMP-19.01 hal.4 No.14 |
| 1.4 | **Bangunan/lantai berpijak rebah atau roboh** (seluruh/sebagian) akibat kegagalan komponen/beban | A | Inspeksi Area Kerja oleh tim Safety/PNC/ERG/DIC mitra kerja sebelum kerja dimulai | Deteksi struktural terbatas pada inspeksi visual berkala, bukan pengujian struktur mendalam | S-CMP-19.02 hal.1 baris 11; S-CMP-19.01 hal.6 No.3 |
| 1.5 | **Tersengat listrik** saat bekerja ketinggian dekat instalasi bertegangan | A | Identifikasi bahaya listrik wajib tercantum dalam JSA; koordinasi LOTO bila tumpang tindih dengan pekerjaan listrik | Risiko tetap ada bila zona kerja listrik di sekitar area ketinggian tidak teridentifikasi penuh dalam JSA | S-CMP-19.02 hal.1 baris 10 |
| 1.6 | **Barang bawaan jatuh** menimpa orang di area bawah | A | Pembatas area kerja/demarkasi & rambu kegiatan dipasang di sekitar/di bawah lokasi kerja ketinggian | Barang kecil/lepas yang tidak terikat tetap berpotensi jatuh; tidak ada kontrol fisik tambahan (jaring/tool lanyard) disebutkan eksplisit | S-CMP-19.02 hal.1–2 baris 12; S-CMP-19.01 hal.4 No.17,19 |
| 1.7 | **Kegagalan platform/papan pijakan** menahan beban karena bukan dari material besi | R | Persyaratan platform/papan pijakan wajib terbuat dari material besi | Kegagalan platform besi akibat korosi/cacat produksi bila tidak diperiksa berkala | S-CMP-19.02 hal.2 baris 13 |
| 1.8 | Cedera/jatuh akibat **posisi kerja tidak ergonomis** atau **hilang fokus** (aktivitas lain selain pekerjaan) | A | Pengawasan melekat oleh Pengawas Layer 1; Papan Komitmen ditandatangani sebelum & setiap perulangan aktivitas | Pelanggaran perilaku individu yang lolos dari pengawasan sesaat | S-CMP-19.02 hal.2 baris 14–15; S-CMP-19.01 hal.4 No.13 |
| 1.9 | Visibilitas rendah saat **kerja ketinggian malam hari** | A | Wajib persetujuan KTT untuk kerja ketinggian malam hari | Risiko visibilitas tetap ada meski disetujui, bergantung pencahayaan tambahan aktual di lapangan | P-CMP-19 §4.4.2.1 poin 1 |
| 1.10 | Pingsan/jatuh akibat **kondisi kesehatan tidak layak** (tekanan darah, dll.) | A | Pemeriksaan kesehatan minimal tekanan darah oleh paramedic sebelum kerja ketinggian | Kondisi kesehatan dapat berubah mendadak selama shift setelah pemeriksaan awal | P-CMP-19 §4.4.2.1 poin 5 |

---

## 2. Kerja Dekat/Atas Air (IKDA)

**Aktivitas:** Pekerjaan dekat air atau di atas air dengan kedalaman >1 meter, pada area tanpa pagar pengaman tinggi minimal 90 cm. *(P-CMP-19 §3.12)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 2.1 | **Tenggelam** karena personil tidak menggunakan pelampung | APD | Pelampung/Life Jacket wajib dipakai; Ringbuoy tersedia di lokasi | Pelampung tidak efektif jika ukuran tidak sesuai atau tidak dikenakan dengan benar | P-CMP-19 §3.12; S-CMP-19.01 hal.1 No.7,10; S-CMP-19.02 hal.1 baris 7 |
| 2.2 | **Jatuh dari platform kerja** di atas air yang tidak memadai | R | Jembatan kerja dengan balok apung HDPE + handrail sepanjang jembatan | Platform sementara/darurat yang belum memenuhi spesifikasi jembatan standar | S-CMP-19.02 hal.1 baris 8; S-CMP-19.01 hal.3 No.10 |
| 2.3 | **Tenggelam/terjebak dalam unit A2B** (excavator/dozer) yang bekerja dekat/atas air jika unit terperosok | R + APD | Emergency exit unit wajib berfungsi; unit tidak dilengkapi wiremesh (agar akses darurat terbuka); pelampung + palu pemecah kaca + alat pemotong seat belt disediakan pengawas; assessment geoteknik pada dudukan unit | Kegagalan evakuasi darurat tetap mungkin bila waktu respons tidak cukup atau unit terbalik sepenuhnya | P-CMP-19 §4.4.2.2 poin 3 |
| 2.4 | **Kebakaran** akibat material mudah terbakar di lokasi kerja dekat air | A | Inspeksi area kerja sebelum mulai untuk mendeteksi & menyingkirkan material mudah terbakar | Material baru dapat masuk lokasi setelah inspeksi awal selesai | S-CMP-19.02 hal.1 baris 9 |
| 2.5 | Tenggelam/tersesat akibat **kerja malam hari** dengan visibilitas rendah | A | Larangan kerja dekat/atas air malam hari, kecuali pekerjaan rutin yang dikecualikan (pengapuran WMP, perawatan sump, mooring, dll.) | Pekerjaan rutin yang dikecualikan tetap dilakukan malam hari tanpa kontrol tambahan spesifik | P-CMP-19 §4.4.2.2 poin 1–2 |
| 2.6 | **Bahaya tak terduga lainnya** di sekitar area kerja (arus, benda tajam bawah air, dll.) belum dikendalikan | A | Assessment Geoteknik Dudukan Unit, Inspeksi Area Kerja, JSA | Bahaya bawah permukaan air sulit terdeteksi visual sepenuhnya | S-CMP-19.02 hal.1 baris 10 |
| 2.7 | Risiko fisik tambahan pada **kerja "di dalam air"** | A | Wajib kajian teknis DIC + persetujuan KTT sebelum pengajuan ijin kerja | Kajian teknis bersifat administratif; tidak menghilangkan risiko fisik pekerjaan bawah air itu sendiri | P-CMP-19 §4.4.2.2 poin 4 |

---

## 3. Kerja Ruang Terbatas (IKRT)

**Aktivitas:** Pekerjaan tidak rutin dengan sirkulasi udara terbatas, potensi keracunan gas, tanpa penerangan permanen, potensi terperangkap, akses masuk=keluar, atau pergerakan personil terbatas. *(P-CMP-19 §3.13)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 3.1 | **Keracunan/asfiksia** akibat Gas Atmosfer Berbahaya (O₂ di luar 19,5–23,5%; gas mudah terbakar >10% LEL; gas beracun >NAB — lihat tabel kandungan gas) | R + A + APD | Blower/Ventilator untuk sirkulasi paksa; Gas Detektor & Personal Gas Meter terkalibrasi berkala; pengujian awal gas atmosfer wajib + pemantauan berkala sesuai durasi tabel suhu; Respirator/SCBA sebagai lapisan terakhir | Keterlambatan deteksi bila alat gagal kalibrasi atau interval pemantauan terlewat | P-CMP-19 §3.13.2, §4.4.2.3 poin 4–6, tabel kandungan gas hal.18; S-CMP-19.01 hal.2–3 No.7,9,16 |
| 3.2 | **Terperangkap tanpa jalur evakuasi** (akses masuk = akses keluar) | A | Petugas K3 Penyelamat Ruang Terbatas ditunjuk; Rescue Plan wajib dilampirkan; titik kumpul/assembly point & jalur evakuasi ditentukan dalam desain pekerjaan | Waktu evakuasi tetap dibatasi geometri ruang sempit itu sendiri | P-CMP-19 §3.13.4–5; S-CMP-19.01 hal.6 No.11 |
| 3.3 | **Heat stress** pada suhu tinggi ruang terbatas | A | Pembatasan lama pajanan sesuai tabel suhu (30°C/180 menit s.d. 44°C/15 menit); pengukuran ulang tiap 15 menit | Variasi toleransi individu terhadap panas tidak sepenuhnya terakomodasi batas waktu generik | P-CMP-19 hal.17 (tabel suhu) |
| 3.4 | **Kebakaran/ledakan** akibat gas mudah terbakar terakumulasi | R + A | Penerangan wajib explosion-proof; larangan api terbuka bila ruang mengandung gas terbakar; ventilasi pembuangan gas berbahaya | Akumulasi gas dapat terjadi cepat jika ventilasi terhenti tanpa disadari | P-CMP-19 §4.4.2.3 poin 7–8 |
| 3.5 | Bekerja pada **kondisi pencahayaan/oksigen tidak memadai** tanpa terdeteksi | A | STOP otomatis bila pencahayaan <80 lux atau oksigen tidak cukup; Teknisi Deteksi Gas bertugas khusus tanpa merangkap tugas lain | — | S-CMP-19.02 hal.1 baris 6–8 |
| 3.6 | Deteksi bahaya lebih rendah saat **kerja malam hari** | A | Larangan mutlak kerja ruang terbatas malam hari | — | P-CMP-19 §4.4.2.3 poin 1 |

---

## 4. Kerja Pengangkatan & Pengangkutan Material (IKPM)

**Aktivitas:** Pengangkatan vertikal (excavator/loader melebihi kabin, radius swing terbatas, penggunaan crane, >1 alat angkat) dan pengangkutan horizontal (dimensi/ketinggian melebihi standar, alat tidak sesuai SKO). *(P-CMP-19 §3.14)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 4.1 | **Beban jatuh/putus** karena melebihi kapasitas SWL alat angkat | R + A | Alat bantu angkat (chain/webbing/wire/shackle) sesuai kapasitas dengan SWL terlihat jelas; Metode Pengangkatan mencakup perhitungan beban material | Kesalahan estimasi berat aktual material di lapangan | S-CMP-19.02 hal.1 baris 7; S-CMP-19.01 hal.2 No.6 |
| 4.2 | **Material lepas/bergeser** saat pengangkatan/pengangkutan karena pengikatan tidak sesuai metode | A | Metode Pengangkatan/Pengangkutan mencakup metode pengikatan; material diikat kuat & diberi tanda pada bagian menonjol | Kegagalan pengikatan akibat human error tetap mungkin terjadi | S-CMP-19.02 hal.1 baris 8; P-CMP-19 §4.4.2.4 poin 6 |
| 4.3 | **Tertimpa/tergilas** karena berada di bawah radius swing alat angkat | R + A | Pembatas area kerja/demarkasi di sekitar radius swing; pengawasan langsung memastikan area bebas personil | Pelanggaran batas oleh pihak ketiga yang tidak terkontrol penuh | S-CMP-19.02 hal.1 baris 9 |
| 4.4 | **Unit rebah/amblas** karena penempatan tidak sesuai kondisi tanah | R + A | Inspeksi area kerja sebelum pengangkatan (unit rata, tidak ada potensi amblas, tidak hujan); SKO unit masih berlaku | Kondisi tanah dapat berubah (hujan mendadak, pergerakan tanah) setelah inspeksi awal | S-CMP-19.02 hal.1 baris 10; P-CMP-19 §4.4.2.4 poin 5 |
| 4.5 | **Tabrakan dengan pengguna jalan lain** selama pengangkutan | A | Pengawalan dengan komunikasi radio ke pengguna jalan lain setiap 15 menit; rambu jarak aman ramp door | Kepatuhan pengguna jalan lain berada di luar kendali langsung | P-CMP-19 §4.4.2.4 poin 7–8 |
| 4.6 | **Bongkar-muat tidak terkendali** oleh unit transportir luar area tanpa SKO | E | Larangan mutlak unit luar daerah operasi melakukan bongkar-muat sendiri; wajib menggunakan unit ber-SKO di area operasi | — | P-CMP-19 §4.4.2.4 poin 2 |
| 4.7 | **Penyimpangan pelaksanaan** dari rencana pengangkatan yang sudah ditetapkan | A | Personil wajib menjalankan Lifting Plan yang disetujui; pengawasan langsung | Penyimpangan sepihak operator di lapangan | S-CMP-19.02 hal.2 baris 11 |

---

## 5. Kerja Panas (IKDP)

**Aktivitas:** Pekerjaan menggunakan panas/api (pengelasan, pemotongan, penggerindaan yang menimbulkan percikan) di luar welding bay. *(P-CMP-19 §3.15)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 5.1 | **Kebakaran** akibat percikan api mengenai bahan bakar/material mudah terbakar | R + A | Jarak minimum 5 meter material pengelasan–bahan bakar + welding screen; larangan pengelasan dekat bahan mudah terbakar; penyingkiran material mudah terbakar dari lokasi | Percikan dapat melompat lebih jauh dari radius aman tergantung kondisi angin | P-CMP-19 §4.4.2.5 poin 1; S-CMP-19.02 hal.1 baris 8–9 |
| 5.2 | **Ketidakmampuan mengendalikan kebakaran** bila terjadi | R | APAR tersedia di lokasi kerja panas | Efektivitas APAR terbatas pada skala kebakaran kecil | S-CMP-19.02 hal.1 baris 7 |
| 5.3 | **Ledakan/kebocoran tabung gas** bertekanan | R | Pressure gauge/regulator baik, flash back arrestor berfungsi; penyimpanan dalam kerangkeng terpisah isi/kosong, jarak minimal 6 meter antar tabung oxygen–acetylene yang berisi | Kegagalan komponen internal tabung tidak selalu terdeteksi inspeksi visual | P-CMP-19 §4.4.2.5 poin 4; S-CMP-19.01 hal.4 No.26 |
| 5.4 | **Luka bakar/cedera mata** akibat percikan las | APD | Jaket Las/Apron, Kaca Mata, Pelindung Wajah, Sarung Tangan Las, Topeng Las wajib | Bergantung kepatuhan pemakaian & kondisi APD tidak aus | S-CMP-19.01 hal.1 (Matriks APD Panas) |
| 5.5 | **Cedera akibat mesin gerinda** (pecahan batu gerinda, dll.) | R | Safety guard/shield pada mesin gerinda; RPM batu gerinda harus lebih besar dari RPM mesin; P2H sebelum digunakan | Kegagalan komponen batu gerinda akibat cacat produksi | S-CMP-19.01 hal.3 No.12 |

---

## 6. Kerja Listrik (IKDL)

**Aktivitas:** Pemasangan dan pemeliharaan instalasi tenaga listrik bertegangan >50 Volt (AC & DC) dan/atau dekat bagian bertegangan. *(P-CMP-19 §3.16)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 6.1 | **Tersengat listrik (electrocution)** akibat kontak dengan instalasi bertegangan | R + A + APD | Isolasi energi (LOTO) wajib selama pekerjaan; bila LOTO tidak dapat dilakukan (mis. penyambungan ke jaringan utama) mengikuti ketentuan khusus; Sarung Tangan Listrik + Helm dengan tali pengikat + Sepatu Keselamatan | Risiko tetap ada pada kondisi kerja bertegangan (live-line work) di mana LOTO tidak dapat diterapkan penuh | P-CMP-19 §4.4.2.6 poin a; S-CMP-19.02 hal.1 baris 7,10 |
| 6.2 | **Jatuh saat memanjat tiang listrik** | R + APD | Alat Panjat Tiang Listrik dengan full body harness double lanyard + penahan pinggang, anchor strap, connecting rope, pengunci pijakan kaki anti-korosif, karet anti-slip | Kegagalan komponen alat panjat akibat keausan yang tidak terdeteksi | S-CMP-19.01 hal.3 No.1 |
| 6.3 | **Kontrol terlambat/tidak konsisten** karena pencatatan administrasi IKDL masih manual | A | Formulir Izin Bekerja dengan Listrik (F-CMP-19.09) tetap wajib diisi & diverifikasi Pengawas Teknis meski manual; verifikasi lapangan tetap wajib untuk IKDL meski umumnya Skema 1 tanpa assessment lapangan | Proses manual lebih rentan keterlambatan/kehilangan dokumen dibanding sistem digital HSE Automation | P-CMP-19 hal.2 ("Perlu diingat"); §4.4.1.1 poin d |

---

## 7. Kerja di Luar Workshop (IKDW)

**Aktivitas:** Pekerjaan di luar workshop yang berpotensi menimbulkan kecelakaan lingkungan kategori sedang/berat dengan sumber pencemaran limbah B3/material B3. *(P-CMP-19 §3.10)*

| No | Risiko | Jenis Pengendalian | Pengendalian yang Dilakukan | Risiko Sisa | Referensi Sumber |
|---|---|---|---|---|---|
| 7.1 | **Pencemaran lingkungan** (tumpahan/release limbah B3) kategori sedang–berat (cair 50–40.000 liter / padat 1–100 m³) | R + A | Spill Kit (absorbent paper, oil boom, oil dispersant), Terpal & Tray/Drum Penampung untuk menampung tumpahan; eskalasi wajib ke IKK (bukan cukup DOP) bila potensi ≥ kategori sedang | Efektivitas penampungan bergantung kecepatan respons & deteksi tumpahan awal | P-CMP-19 §3.10, tabel kategori insiden hal.4; S-CMP-19.01 hal.2 No.20–22 |
| 7.2 | Paparan langsung terhadap bahaya fisik dasar (bukan risiko lingkungan) di area luar workshop | APD | Helm, Kaca Mata, Sepatu Keselamatan, Sarung Tangan Kain wajib | Tidak mengendalikan risiko pencemaran lingkungan itu sendiri — hanya melindungi individu | S-CMP-19.01 hal.1 (Matriks APD Luar Workshop) |
| 7.3 | Kondisi aktual lokasi tidak tercermin karena verifikasi tanpa assessment lapangan (Skema 1) | A | Pemeriksaan dokumen oleh Pengawas Teknis sebelum pengajuan online; IKDW tidak dieskalasi ke verifikasi lapangan Skema 2 | Risiko lapangan yang tidak tercermin dalam dokumen tidak terverifikasi secara langsung | P-CMP-19 §3.2 |

---

## Tabel Performance Pengawas (Pengendalian Administratif atas Risiko U6)

Sistem sanksi bertingkat ini merupakan **pengendalian administratif** terhadap risiko "kegagalan fungsi pengawasan" (lihat baris U6 di atas) — bersifat reaktif, diterapkan setelah ketidaksesuaian teridentifikasi.

| Deskripsi Ketidaksesuaian | Kategori | Tahap 1 | Tahap 2 | Tahap 3 |
|---|---|---|---|---|
| APD tidak layak digunakan | Minor | Coaching Kabag | Coaching PJO | Suspend KPO Safety 1 bulan |
| Peralatan tidak layak digunakan | Minor | Coaching Kabag | Coaching PJO | Suspend KPO Safety 1 bulan |
| Pengawas/Pekerja tidak terdaftar dalam pengajuan IKK | Minor | Coaching Kabag | Coaching PJO | Suspend KPO Safety 1 bulan |
| Pengawas langsung tidak berada di lokasi pekerjaan | Medium | Coaching PJO | Suspend KPO Safety 1 bulan | Suspend KPO Safety 2 bulan |
| Tidak paham teknis pekerjaan/JSA | Medium | Coaching PJO | Suspend KPO Safety 1 bulan | Suspend KPO Safety 2 bulan |
| Pengawas langsung tidak melakukan OAK | Medium | Coaching PJO | Suspend KPO Safety 1 bulan | Suspend KPO Safety 2 bulan |
| Pengawas dan/atau Pekerja tidak kompeten | Major | Suspend KPO Safety 3 bulan (langsung) | — | — |
| Melakukan pekerjaan tanpa surat ijin kerja khusus | Major | Suspend KPO Safety 3 bulan (langsung) | — | — |

*Referensi: S-CMP-19.01 hal.7*

---

## Dokumen Terkait (Referensi Formulir per Aktivitas)

| Nomor | Nama Dokumen | Masa Simpan | Aktivitas Terkait |
|---|---|---|---|
| F-CMP-19.01 | Formulir Inspeksi Pra Kerja IKK Di Luar Workshop | 2 Tahun | IKDW |
| F-CMP-19.02 | Formulir Inspeksi Pra IKK Dekat/Atas Air | 2 Tahun | IKDA |
| F-CMP-19.03 | Formulir Inspeksi Pra Kerja IKK Ketinggian | 2 Tahun | IKDK |
| F-CMP-19.04 | Formulir Inspeksi Pra Kerja IKK Listrik | 2 Tahun | IKDL |
| F-CMP-19.05 | Formulir Inspeksi Pra Kerja IKK Panas | 2 Tahun | IKDP |
| F-CMP-19.06 | Formulir Inspeksi Pra Kerja IKK Pengangkatan dan Pengangkutan Material | 2 Tahun | IKPM |
| F-CMP-19.07 | Formulir Inspeksi Pra Kerja IKK Ruang Terbatas | 2 Tahun | IKRT |
| F-CMP-19.08 | Formulir Pengujian Gas Atmosfer | 2 Tahun | IKRT |
| F-CMP-19.09 | Formulir Izin Bekerja dengan Listrik | 2 Tahun | IKDL |
| F-CMP-19.10 | Formulir Daily Operation Plan Maintenance | 2 Tahun | Umum |

*Referensi: P-CMP-19 hal.22 (Bab 5. Dokumen Terkait)*
