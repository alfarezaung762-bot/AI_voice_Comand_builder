# 40 Kombinasi Parameter ElevenLabs untuk Dataset Edge Impulse

Berikut adalah **40 kombinasi parameter** yang telah dirancang secara sistematis untuk menghasilkan dataset audio tiruan (synthetic) yang kaya akan variasi. Menggunakan variasi ini sangat krusial saat melatih model Keyword Spotting (KWS) pada **Edge Impulse** (target **ESP32-S3**) agar model tangguh di dunia nyata, memiliki akurasi deteksi tinggi, dan **bebas dari overfitting**.

Seluruh kombinasi di bawah disetel agar durasi kata perintah tetap berada di dalam batas aman **maksimal 2 detik**.

---

## Tabel 40 Kombinasi Parameter

| No | Kategori / Varian | Stability | Clarity (Similarity) | Style Exaggeration | Speed | Language Override | Alasan & Tujuan Simulasi |
|:---|:---|:---:|:---:|:---:|:---:|:---:|:---|
| **1** | Normal ID (Baseline) | 60% | 75% | 0% | 100% | `id` (Indonesia) | Baseline suara normal dengan logat Indonesia standar. |
| **2** | Ekspresif ID | 35% | 60% | 45% | 100% | `id` (Indonesia) | Intonasi dinamis, mirip cara bicara santai sehari-hari. |
| **3** | Aksen Inggris | 55% | 75% | 10% | 100% | `en` (Inggris) | Aksen barat (inggris-sentris) untuk variasi pelafalan huruf vokal. |
| **4** | Aksen Jepang | 50% | 70% | 15% | 100% | `ja` (Jepang) | Pelafalan dengan aksen Asia Timur (biasanya vokal lebih tegas/kaku). |
| **5** | Aksen Spanyol | 50% | 70% | 20% | 100% | `es` (Spanyol) | Logat Eropa Selatan dengan intonasi ucapan yang lebih bergelombang. |
| **6** | Aksen Arab | 55% | 70% | 15% | 100% | `ar` (Arab) | Simulasi penekanan tenggorokan (konsonan tajam). |
| **7** | Aksen Jerman | 60% | 75% | 10% | 100% | `de` (Jerman) | Karakter bicara tegas, keras, dan artikulasi huruf mati yang solid. |
| **8** | Cepat Normal | 65% | 70% | 0% | 115% | `id` (Indonesia) | Simulasi pengucapan cepat (misal saat terburu-buru). |
| **9** | Cepat Aksen | 50% | 70% | 20% | 120% | `en` (Inggris) | Sangat cepat beraksen Inggris untuk melatih toleransi tempo cepat. |
| **10** | Lambat Normal | 60% | 75% | 0% | 85% | `id` (Indonesia) | Pengucapan lambat/seret untuk melatih toleransi tempo lambat. |
| **11** | Lambat Aksen | 55% | 70% | 15% | 80% | `en` (Inggris) | Lambat beraksen Inggris (pengucapan terseret). |
| **12** | Karakter Lain 1 | 40% | 35% | 50% | 100% | `id` (Indonesia) | Clarity rendah mengubah karakteristik pitch, mensimulasikan orang lain. |
| **13** | Karakter Lain 2 | 45% | 30% | 60% | 100% | `en` (Inggris) | Karakter suara orang lain beraksen Inggris. |
| **14** | Sangat Variatif | 15% | 60% | 30% | 105% | `id` (Indonesia) | Stabilitas sangat rendah membuat intonasi tiap *take* berbeda jauh. |
| **15** | Tegas / Emosional | 30% | 65% | 80% | 110% | `id` (Indonesia) | Pengucapan dengan penekanan emosi tinggi/kencang. |
| **16** | Flat / Monoton | 95% | 80% | 0% | 95% | `id` (Indonesia) | Suara sangat datar tanpa ekspresi (simulasi suara robotik/mengantuk). |
| **17** | Bisik Cepat | 20% | 40% | 70% | 115% | `id` (Indonesia) | Bisikan cepat, melatih deteksi saat pengguna berbisik dekat mic. |
| **18** | Bisik Lambat | 30% | 45% | 50% | 85% | `ja` (Jepang) | Bisikan lambat beraksen Asia (desisan angin lebih dominan). |
| **19** | Suara Jauh / Samar | 50% | 25% | 25% | 105% | `id` (Indonesia) | Clarity 25% mendistorsi vokal asli, mensimulasikan jarak jauh. |
| **20** | Sengau (Nasal) | 40% | 55% | 40% | 110% | `fr` (Prancis) | Logat Prancis memberikan efek sengau (nasal) pada pengucapan kata. |
| **21** | Aksen Melayu | 55% | 70% | 10% | 100% | `ms` (Malaysia) | Logat melayu serumpun, artikulasi vokal mirip tapi berlogat khas. |
| **22** | Aksen Korea | 50% | 75% | 20% | 95% | `ko` (Korea) | Logat Korea dengan intonasi lembut khas Asia Timur. |
| **23** | Aksen Italia | 50% | 65% | 35% | 105% | `it` (Italia) | Dinamika bicara dinamis, bersemangat, dan berayun khas Italia. |
| **24** | Aksen India | 60% | 75% | 15% | 100% | `hi` (Hindi) | Karakter bunyi konsonan dental "d" dan "t" yang sangat tebal. |
| **25** | Aksen Swedia | 55% | 70% | 20% | 95% | `sv` (Swedia) | Logat Eropa Utara yang melodik/sing-song (tinggi-rendah berirama). |
| **26** | Aksen Vietnam | 40% | 65% | 25% | 105% | `vi` (Vietnam) | Logat Asia Tenggara daratan dengan dinamika nada naik-turun. |
| **27** | Aksen Thailand | 45% | 70% | 20% | 100% | `th` (Thailand) | Pengucapan bernada lembut dan tempo cenderung tenang. |
| **28** | Cepat & Ekspresif | 25% | 60% | 60% | 115% | `id` (Indonesia) | Suara terburu-buru dengan intonasi emosi tinggi. |
| **29** | Lambat & Ekspresif | 30% | 60% | 65% | 85% | `id` (Indonesia) | Gaya bicara dramatis, lambat, namun berenergi tinggi. |
| **30** | Bisik Aksen Arab | 25% | 40% | 50% | 100% | `ar` (Arab) | Bisikan dengan gesekan (frikatif) tenggorokan yang kuat. |
| **31** | Bisik Aksen Jerman | 25% | 45% | 45% | 105% | `de` (Jerman) | Bisikan tajam dengan letupan (plosif) konsonan akhir. |
| **32** | Simulasi Anak-anak | 35% | 45% | 50% | 110% | `id` (Indonesia) | Clarity rendah & speed cepat mensimulasikan pita suara anak kecil. |
| **33** | Simulasi Lansia | 30% | 50% | 40% | 80% | `id` (Indonesia) | Tempo sangat lambat & stabilitas rendah (mensimulasikan suara bergetar). |
| **34** | Suara Berat / Slavia | 70% | 55% | 30% | 90% | `ru` (Rusia) | Suara berat, tegas, tempo tenang dengan timbre Slavia tebal. |
| **35** | Panik / Darurat | 20% | 55% | 75% | 120% | `id` (Indonesia) | Tempo maksimal & stabilitas minim (simulasi saat berteriak meminta tolong). |
| **36** | Suara Bergumam | 15% | 40% | 10% | 95% | `id` (Indonesia) | Stabilitas sangat rendah menghasilkan artikulasi malas/tidak jelas. |
| **37** | Monoton Cepat (Robot)| 98% | 85% | 0% | 115% | `en` (Inggris) | Stabilitas maksimum, tanpa emosi (simulasi asisten AI lain/robot). |
| **38** | Aksen Portugis | 50% | 70% | 25% | 100% | `pt` (Portugis) | Logat Eropa Selatan dengan artikulasi vokal tertutup dan lembut. |
| **39** | Aksen Turki | 55% | 75% | 15% | 95% | `tr` (Turki) | Logat dengan harmonisasi vokal khas bahasa Turki. |
| **40** | Aksen Polandia | 55% | 70% | 20% | 100% | `pl` (Polandia) | Karakter suara dengan bunyi desis sibilant (sz, cz) yang khas. |

---

## Analisis & Spekulasi: Berapa Kombinasi Parameter yang Ideal?

Dalam machine learning untuk **Keyword Spotting (KWS)**, kualitas dan variasi dataset jauh lebih penting daripada sekadar jumlah data mentah.

### 1. Spekulasi Jumlah Kombinasi Maksimal (Diminishing Returns)
* **Batas Maksimal Efektif**: Berdasarkan teori pemrosesan audio digital dan pelatihan neural network (seperti CNN/MobileNet), batas maksimal kombinasi parameter sintetik yang berguna berkisar antara **50 hingga 60 kombinasi**.
* **Alasan**: Jika Anda membuat lebih dari 60 kombinasi, karakteristik audio antarkombinasi akan mulai tumpang tindih (*overlap*) secara signifikan. Model tidak lagi mendapatkan informasi fitur audio baru, melainkan hanya duplikasi informasi, yang justru dapat memperlambat waktu pelatihan dan membuang kuota ElevenLabs Anda.
* **Mengapa 40 Kombinasi adalah Sweet Spot?**:
  40 kombinasi ini telah mencakup seluruh spektrum variasi vokal yang dibutuhkan:
  * **Variasi Waktu (Speed)**: Cepat (115%-120%), Normal (95%-100%), Lambat (80%-85%).
  * **Variasi Pitch & Formant (Clarity & Style)**: Mengubah warna suara tiruan agar terdengar seperti 4-5 orang berbeda.
  * **Variasi Tekstur (Bisikan, Gumaman, Emosi)**: Melatih ketahanan model terhadap cara pengucapan ekstrim.
  * **Variasi Dialek (Language Override)**: 15+ aksen berbeda mengajarkan model untuk fokus pada *fonem inti kata*, bukan pada aksen pembicara.

### 2. Matematika Ekspansi Dataset (Data Augmentation)
Dengan menggunakan 40 kombinasi ini, Anda dapat melipatgandakan data tanpa perlu men-generate ratusan file secara manual:
1. **Pilih 10 Model Suara** (Bawaan + Kustom).
2. **Gunakan 40 Kombinasi** di atas:  
   $$\text{10 suara} \times \text{40 kombinasi} = 400 \text{ file audio unik}.$$
3. **Set Jumlah Variasi (Takes) ke 3 versi** (pada kombinasi stabilitas rendah):  
   Hal ini menghasilkan rata-rata 2.5 takes per kombinasi $\rightarrow 400 \times 2.5 = 1000 \text{ file audio}$.
4. **Data Augmentation di Edge Impulse**:  
   Saat melatih di Edge Impulse, aktifkan fitur penambahan noise latar belakang (*background noise*), pergeseran waktu (*time shift*), dan distorsi frekuensi. Ini akan mengubah 1000 file audio menjadi **3000+ sampel latihan** yang sangat bervariasi.

Ukuran **3000 sampel** dengan keberagaman setinggi ini dijamin membuat model ESP32-S3 Anda sangat responsif terhadap suara siapa pun, dalam situasi apa pun, tanpa mengalami *overfitting*!
