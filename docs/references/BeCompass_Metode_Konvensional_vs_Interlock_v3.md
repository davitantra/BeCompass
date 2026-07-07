# Referensi BeCompass — Metode Pemastian Pengendalian: Konvensional vs Interlock

> Melanjutkan dari `BeCompass_Referensi_Ijin_Kerja_Khusus_v2.md`. Dokumen ini mengkaji **bagaimana memastikan** setiap risiko benar-benar terkendali (bukan sekadar tertulis di prosedur), dengan membandingkan dua pendekatan:
>
> - **Metode Konvensional** — bergantung pada pelaporan/verifikasi manusia (checklist, tanda tangan, observasi visual). Titik lemah: bisa "dibohongi" — dicentang tanpa benar-benar diperiksa.
> - **Metode Interlock** — kontrol fisik/mekanik atau digital/IoT yang **memblokir** pekerjaan berbahaya berlanjut jika syarat belum terpenuhi, tanpa bergantung kejujuran individu. Interlock dibagi dua sub-jenis di sini: **Interlock Fisik/Mekanik** (murni hardware) dan **Interlock Digital/IoT** (sensor + software, sejalan arah pengembangan BeCompass).
>
> Nomor risiko mengacu ke `..._v2.md`. Untuk risiko yang secara realistis tidak bisa dibuatkan interlock sempurna, dicari alternatif terdekat dan diberi catatan keterbatasannya.

---

## Ketentuan Umum Lintas Aktivitas (U1–U6)

| No | Risiko Sisa (ringkas) | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| U1 | Personil tak terdaftar ikut bekerja tanpa terdeteksi | Verifikasi manual daftar personil oleh pengawas saat briefing/IPK | **Digital:** akses masuk area kerja via scan RFID/QR/biometrik personil yang divalidasi otomatis terhadap daftar IKK aktif di sistem; gate/turnstile fisik terkunci bila ID tidak terdaftar | Sangat feasible di titik akses tertutup (gate, pintu); untuk area tambang terbuka luas, gunakan geofencing + alert real-time ke CCR (soft interlock, bukan block fisik penuh) |
| U2 | Pekerjaan dimulai meski IPK belum sesuai | Pengawas mengisi & menandatangani form IPK manual | **Digital:** status ijin kerja digital tidak bisa "Aktif" kecuali 5 parameter IPK diisi "Sesuai" oleh akun pengawas dengan GPS check-in di radius lokasi kerja | Software gate ini kuat untuk mencegah "aktivasi tanpa IPK", tapi tetap perlu integrasi ke hardware alat kritis agar benar-benar memblokir fisik (lihat interlock spesifik per alat) |
| U3 | APD tidak dipakai dengan benar | Observasi visual pengawas (OKK tiap 3 jam), self-declaration | **Digital:** BLE/RFID tag pada APD kritis (harness, respirator) terhubung access point — akses ke zona kerja berisiko tinggi terkunci tanpa tag APD aktif terdeteksi pada tubuh | Feasible untuk APD kritis bernilai tinggi (harness, gas mask); tidak ekonomis untuk semua APD generik (sarung tangan, kacamata) — tetap perlu spot-check konvensional untuk itu |
| U4 | Peralatan tidak layak tapi tetap dipakai | P2H manual dengan form checklist ditandatangani | **Fisik:** interlock mekanik bawaan pabrikan (micro-switch guard, load-limit cut-off) — banyak alat berat modern sudah punya ini secara built-in | Kuncinya bukan membuat baru, tapi **memastikan interlock pabrikan tidak di-bypass** — tambahkan log sensor status ke CCR sebagai lapisan digital verifikasi non-bypass |
| U5 | Dokumen kerja tidak sesuai kondisi aktual | Review manual JSA vs lapangan oleh pengawas/verifikator | **Digital (mendekati):** wajib foto lokasi dengan geotag+timestamp tidak dapat diedit saat submit JSA, dibandingkan otomatis dengan foto referensi lokasi terdaftar | Bukan interlock sejati (masih butuh judgment isi dokumen), tapi mempersulit pemalsuan lokasi/waktu verifikasi |
| U6 | Pengawas tidak menjalankan kewajiban (IPK/OKK/closing) | Laporan manual, sanksi berjenjang setelah temuan (reaktif) | **Digital:** ijin kerja otomatis berubah status "SUSPENDED" jika tidak ada input observasi dengan GPS pengawas dalam 3 jam terakhir; auto-eskalasi notifikasi ke atasan/WKTT | Cukup kuat karena butuh kehadiran fisik pengawas terverifikasi GPS, bukan sekadar klik dari jarak jauh |

---

## 1. Kerja di Ketinggian (IKDK)

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 1.1 | Jatuh karena anchor/hook tidak dikaitkan benar | Pengawas cek visual, self-check pekerja | **Fisik:** *Self-Retracting Lifeline (SRL)*/fall arrestor — mengunci otomatis saat terjadi jatuh bebas. **Digital:** sensor hall-effect pada hook terhubung solenoid lock di akses tangga/perancah/manlift | SRL adalah interlock mekanik matang & terbukti — prioritaskan ini dulu; smart-hook sensor adalah pengembangan lanjutan |
| 1.2 | Jatuh/tergelincir akibat cuaca buruk | Pengawas memantau cuaca manual | **Digital:** anemometer/rain sensor di lokasi kerja, otomatis kirim sinyal STOP & mengunci status ijin digital jadi "SUSPENDED" bila ambang terlampaui | Feasible — sudah lazim dipakai pada operasi crane (wind cut-off otomatis) |
| 1.3 | Keruntuhan perancah | Assessment visual + Scaffold Tag Hijau manual | **Digital:** RFID/QR tag per unit perancah discan inspektor, status otomatis update ke sistem; gembok elektronik akses tangga perancah tidak terbuka tanpa status "Tag Hijau — Valid Hari Ini" | Feasible untuk perancah dengan titik akses jelas |
| 1.4 | Bangunan berpijak roboh | Inspeksi visual tim Safety/ERG | **Digital (terbatas):** strain gauge/tilt sensor pada struktur kritis, alarm otomatis bila deformasi melebihi ambang | Feasible untuk struktur permanen bernilai tinggi; tidak praktis untuk platform sementara biasa — treat sebagai risk-based decision |
| 1.5 | Tersengat listrik di ketinggian | JSA identifikasi bahaya, LOTO manual | **Fisik:** electronic multi-lock LOTO — lihat detail di 6.1 | Sama teknologi dengan kasus IKDL |
| 1.6 | Barang bawaan jatuh menimpa | Pembatas area + rambu manual | **Fisik:** *tool tethering* (tali pengikat alat ke tubuh/struktur) — secara mekanis mencegah alat jatuh bebas meski terlepas dari tangan | Sangat feasible, murah, sudah standar *dropped object prevention* di industri migas/tambang |
| 1.7 | Platform gagal (bukan material besi) | Pemeriksaan visual material sebelum digunakan | **Fisik:** load cell/sensor beban pada platform, alarm/lock otomatis bila overload | Interlock lebih cocok untuk deteksi overload; kesesuaian *material* platform tetap kontrol procurement (hanya boleh beli/pakai platform bersertifikat) |
| 1.8 | Ergonomi buruk / distraksi | Pengawasan visual, papan komitmen self-declaration | **Digital (soft):** wearable sensor (vest/smartwatch) deteksi postur ekstrem atau pola gerak tidak wajar, auto-alert ke pengawas | Bukan hard-block, tapi closed-loop monitoring berbasis sensor objektif — sudah ada di industri tambang (fatigue/posture monitoring) |
| 1.9 | Kerja malam hari, visibilitas rendah | Persetujuan tertulis KTT manual | **Digital:** software approval-gate — ijin tidak bisa "Aktif" untuk jam malam tanpa digital sign-off KTT + verifikasi lux sensor lokasi | Feasible sebagai software workflow gate |
| 1.10 | Kondisi kesehatan tidak layak | Pemeriksaan tekanan darah manual oleh paramedic | **Digital:** alat ukur tekanan darah digital di pos IPK, data otomatis submit ke sistem (bukan input manual); opsional wearable heart-rate/BP real-time selama kerja | Feasible, perlu investasi device tambahan di titik kerja |

---

## 2. Kerja Dekat/Atas Air (IKDA)

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 2.1 | Tenggelam (tidak pakai pelampung) | Pengawas cek visual pemakaian pelampung | **Digital:** RFID/BLE tag pada pelampung terhubung access point area kerja dekat air | Feasible di titik akses terbatas (jetty/dermaga); area terbuka luas kombinasikan dengan geofence + wearable alert |
| 2.2 | Jatuh dari platform/jembatan tidak memadai | Inspeksi visual sebelum digunakan | **Fisik/Digital:** load/tilt sensor pada jembatan kerja apung, auto-alarm/lock bila miring/overload | Feasible untuk jembatan kerja permanen; platform darurat sederhana sulit di-instrument |
| 2.3 | Tenggelam dalam unit A2B yang terperosok | Checklist P2H manual cek emergency exit | **Fisik/Digital:** micro-switch sensor pada pintu darurat unit, terhubung immobilizer — unit tidak bisa di-*starter* jika sensor pintu darurat gagal fungsi | Feasible untuk alat berat modern yang sudah punya sistem start-up terprogram |
| 2.4 | Kebakaran material mudah terbakar dekat air | Inspeksi area visual sebelum kerja | **Digital:** gas/vapor sensor mendeteksi uap mudah terbakar, mengunci aktivasi peralatan panas terdekat (lihat 5.1) | Relevan hanya jika bertumpang tindih dengan hot work; untuk material padat biasa tetap kontrol administratif |
| 2.5 | Kerja malam hari | Larangan manual kecuali daftar pekerjaan rutin dikecualikan | **Digital:** software time-gate pada ijin kerja digital | Feasible, sama pola dengan 1.9 |
| 2.6 | Sumber bahaya lain belum dikendalikan | JSA, inspeksi area kerja manual | **Digital (mendekati):** mandatory photo + checklist digital sebelum submit ijin | Bukan interlock sejati untuk bahaya generik, tapi memperkuat objektivitas verifikasi |
| 2.7 | Risiko fisik kerja "di dalam air" | Kajian teknis manual + persetujuan KTT tertulis | **Digital:** software approval-gate (KTT digital sign-off wajib) | Feasible sebagai gate administratif; tidak menghilangkan risiko fisik ekstrem pekerjaan itu sendiri |

---

## 3. Kerja Ruang Terbatas (IKRT)

> Kategori ini punya potensi interlock paling matang — teknologi *confined space gas monitoring interlock* sudah lazim & terbukti di industri.

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 3.1 | Keracunan/asfiksia akibat gas atmosfer berbahaya | Pengujian awal gas manual dengan gas detector, dicatat form | **Digital:** akses masuk (manhole/pintu) dilengkapi *electronic lock* yang hanya terbuka jika pembacaan gas real-time tetap dalam ambang **secara kontinu** selama pekerjaan; deviasi memicu alarm + exhaust fan otomatis | **Sangat direkomendasikan** — teknologi matang, prioritas tertinggi untuk investasi interlock BeCompass |
| 3.2 | Terperangkap tanpa jalur evakuasi | Rescue plan manual, penunjukan petugas penyelamat | **Digital:** sensor okupansi (RFID scan masuk/keluar) menampilkan real-time jumlah & identitas personil di dalam ke petugas standby | Feasible, sudah ada sebagai *confined space tracking system* di industri |
| 3.3 | Heat stress pada suhu tinggi | Pengukuran suhu manual tiap 15 menit | **Digital:** sensor suhu kontinu + software hitung otomatis akumulasi lama pajanan sesuai tabel, mandatory-exit alarm otomatis saat batas tercapai | Feasible, bisa dikombinasikan wearable body-temperature sensor untuk validasi individual |
| 3.4 | Kebakaran/ledakan gas terakumulasi | Larangan api terbuka manual, penerangan explosion-proof (spek pengadaan) | **Digital:** gas detector terhubung otomatis mematikan sumber ignition non-explosion-proof di area saat kadar gas mudah terbakar melebihi ambang | Mature technology (mirip *ATEX zone interlock*), sangat feasible bila ada anggaran instrumentasi |
| 3.5 | Kerja pada pencahayaan/oksigen tidak memadai | STOP manual berdasarkan observasi | **Digital:** terintegrasi dengan 3.1 (gas/O2 lock) + lux sensor otomatis sebagai syarat status ijin aktif | Feasible, terintegrasi dengan interlock 3.1 |
| 3.6 | Kerja malam hari | Larangan manual | **Digital:** software time-gate | Feasible, pola sama dengan 1.9 |

---

## 4. Kerja Pengangkatan & Pengangkutan Material (IKPM)

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 4.1 | Beban jatuh melebihi SWL | Perhitungan manual beban + SWL terlihat jelas di alat | **Fisik:** *Load Moment Indicator (LMI)/Rated Capacity Indicator (RCI)* — otomatis memotong fungsi hoist/boom bila beban melebihi SWL | **Sangat feasible** — mature engineering interlock, wajib pada banyak regulasi crane modern; pastikan tidak di-*bypass* |
| 4.2 | Material lepas/bergeser (rigging salah) | Pemeriksaan visual pengikatan oleh pengawas | **Digital (soft):** load cell pada sling mendeteksi *uneven load*, alarm otomatis ke operator sebelum lift dimulai | Meningkatkan deteksi dini, tapi tidak menggantikan kompetensi rigger — bukan hard-block murni |
| 4.3 | Tertimpa di bawah radius swing | Pembatas area manual + pengawasan visual | **Fisik/Digital:** *proximity/anti-collision sensor* (radar/LiDAR) pada crane, otomatis menghentikan swing jika mendeteksi manusia dalam radius bahaya | **Sangat direkomendasikan** — sudah tren sebagai *Proximity Detection System (PDS)* di tambang |
| 4.4 | Unit rebah/amblas | Inspeksi visual kondisi tanah sebelum kerja | **Fisik:** *outrigger interlock* — sensor tilt/inclinometer mengunci fungsi angkat bila kemiringan unit melebihi ambang | Mature technology, sudah built-in pada banyak mobile crane modern |
| 4.5 | Tabrakan dengan pengguna jalan lain | Pengawalan manual dengan radio tiap 15 menit | **Digital:** GPS real-time + *Collision Avoidance System (CAS)*, auto-alert ke unit lain yang mendekat | Feasible jika infrastruktur CAS sudah/akan tersedia di GMO |
| 4.6 | Bongkar-muat oleh unit tanpa SKO | Verifikasi dokumen SKO manual di pos pemeriksaan | **Digital:** gate/barrier otomatis membaca RFID/QR SKO kendaraan — palang tidak terbuka tanpa SKO valid terdaftar | Sangat feasible, mirip access-control gate yang sudah umum |
| 4.7 | Penyimpangan rencana pengangkatan | Pengawasan visual kepatuhan lifting plan | **Digital:** kombinasi 4.1+4.3 dengan parameter lifting plan sebagai *geofence*/limit digital pada sistem crane | Advanced tapi feasible pada crane dengan sistem digital modern (*programmable zone limiting*) |

---

## 5. Kerja Panas (IKDP)

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 5.1 | Kebakaran akibat percikan api | Jarak 5 m diukur manual, welding screen dipasang manual | **Digital:** gas/heat/smoke detector di sekitar lokasi hot work, alarm otomatis; hot work permit digital dengan *time-limited validity* yang otomatis *expire* | Sensor+suppression feasible di area kritis (dekat tangki BBM); di lapangan terbuka lebih ke deteksi & alarm, bukan block fisik penuh |
| 5.2 | Ketidakmampuan mengendalikan kebakaran | APAR disediakan, dicek kondisi manual | **Digital:** pressure sensor pada APAR — status ijin hot work tidak "Aktif" kecuali APAR terverifikasi tersedia & bertekanan normal (scan RFID tag APAR) | Feasible sebagai digital checklist-gate |
| 5.3 | Ledakan/kebocoran tabung gas | Pemeriksaan visual regulator/flashback arrestor | **Fisik:** *flashback arrestor* itu sendiri adalah interlock mekanik (sudah wajib); tambahan pressure sensor untuk alarm otomatis | Kuncinya di kontrol procurement — pastikan spesifikasi ini wajib dibeli/dipasang |
| 5.4 | Luka bakar akibat APD tidak sesuai | Pengawasan visual pemakaian APD | **Digital (advanced):** RFID tag pada welding mask terhubung sensor proximity mesin las — mesin *lockout* tanpa tag aktif terdeteksi | Teknologi *smart-PPE*, feasible untuk pilot project, bukan prioritas pertama |
| 5.5 | Cedera akibat mesin gerinda | Pemeriksaan visual safety guard sebelum digunakan | **Fisik:** micro-switch interlock pada safety guard — mesin tidak menyala tanpa guard terpasang sempurna | Sering sudah built-in pabrikan modern; kuncinya verifikasi non-*bypass* |

---

## 6. Kerja Listrik (IKDL)

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 6.1 | Tersengat listrik (live-line work) | LOTO manual dengan gembok & tag kertas/personal | **Fisik:** *Electronic Lockout-Tagout* — breaker tidak bisa di-*energize* kembali kecuali seluruh *personal lock* (multi-lock hasp) dilepas individual terverifikasi biometrik/ID; voltage detector otomatis mengunci akses panel bila masih terdeteksi tegangan | **Sangat direkomendasikan** — best practice industri (*permit-required LOTO*), paling relevan karena IKDL saat ini masih manual sepenuhnya |
| 6.2 | Jatuh saat memanjat tiang listrik | Pemeriksaan visual alat panjat sebelum digunakan | **Fisik:** SRL/smart-hook sensor — sama teknologi dengan 1.1 | Feasible |
| 6.3 | Kontrol administratif manual (form kertas F-CMP-19.09) | Form kertas diisi manual | **Digital:** digitalisasi form ke BeCompass dengan *mandatory-field validation* (submit gagal jika field kosong) + timestamp/geotag otomatis tidak dapat diedit | **Paling relevan langsung dengan pengembangan BeCompass** — ini "interlock" terhadap manipulasi data administratif, bukan risiko fisik langsung |

---

## 7. Kerja di Luar Workshop (IKDW)

| No | Risiko Sisa | Metode Konvensional | Metode Interlock | Catatan Feasibility |
|---|---|---|---|---|
| 7.1 | Pencemaran lingkungan (tumpahan B3) | Spill kit disediakan, dicek ketersediaan manual | **Fisik:** *secondary containment* (bund wall/double-wall tank) — kontrol pasif yang otomatis menampung tumpahan tanpa bergantung tindakan manusia; sensor level/leak detection pada tempat penyimpanan B3 untuk alarm otomatis | **Sangat feasible** — bund wall adalah interlock fisik pasif yang sudah standar industri, prioritas tinggi |
| 7.2 | APD dasar tidak memadai | Pengawasan visual | **Digital:** RFID/tag APD access-control (pola sama seperti kasus lain) | Feasible tapi prioritas rendah dibanding risiko utama (pencemaran) |
| 7.3 | Kondisi lapangan tidak tercermin (verifikasi tanpa assessment lapangan) | Pemeriksaan dokumen manual oleh Pengawas Teknis | **Digital (mendekati):** mandatory geotagged photo (timestamp+GPS tidak dapat diedit) sebagai syarat submit ijin digital | Soft interlock, meningkatkan traceability meski bukan interlock fisik murni |

---

## Ringkasan Prioritas Implementasi (untuk Roadmap BeCompass)

Berdasarkan tingkat kematangan teknologi dan dampak risiko, urutan prioritas interlock yang disarankan untuk dikembangkan/diadopsi lebih dulu:

1. **Electronic LOTO** (6.1, 1.5) — teknologi matang, langsung menjawab gap "IKDL masih manual"
2. **Confined space gas-lock system** (3.1, 3.4, 3.5) — teknologi matang, risiko fatal tinggi (asfiksia)
3. **Load Moment Indicator + Proximity Detection System pada alat angkat** (4.1, 4.3, 4.4) — teknologi matang, sudah tren di tambang
4. **Digital IPK/ijin kerja dengan GPS check-in & time-gate** (U1, U2, U6, 1.9, 2.5, 2.7, 3.6) — murni pengembangan software BeCompass, tidak perlu hardware tambahan, ROI cepat
5. **SRL/fall arrestor & tool tethering** (1.1, 1.6, 6.2) — interlock fisik murah & terbukti, mudah diadopsi
6. **Secondary containment B3** (7.1) — kontrol fisik pasif, investasi satu kali
7. Sisanya (smart-PPE RFID, wearable posture/health sensor, sensor struktur) — tahap lanjutan setelah fondasi di atas berjalan, karena butuh investasi lebih besar & belum semasif dampaknya dibanding 6 poin di atas.
