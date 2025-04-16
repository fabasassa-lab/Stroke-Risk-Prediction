# Laporan Proyek Machine Learning Terapan - Achmad Fauzihan Bagus Sajiwo

<div align="center">
	<p>STROKE RISK - PREDICTIVE ANALYSIS</p>
</div>

<div align="center">
	<img src="https://github.com/fabasassa-lab/Stroke-Risk-Prediction/blob/main/image/stroke.png?raw=true">
</div>

## Domain Proyek

Stroke merupakan salah satu penyebab utama kematian dan kecacatan di Indonesia. Menurut studi Global Burden of Disease (GBD) tahun 2019, Indonesia memiliki angka kematian akibat stroke yang tinggi, dengan tingkat kematian yang disesuaikan berdasarkan usia dan jenis kelamin sebesar 193,3 per 100.000 penduduk [1].​

Prevalensi stroke di Indonesia juga menunjukkan tren peningkatan. Data dari Riset Kesehatan Dasar (Riskesdas) tahun 2018 mencatat bahwa prevalensi stroke meningkat dari 7 per 1.000 penduduk pada tahun 2013 menjadi 10,9 per 1.000 penduduk pada tahun 2018 [1].​

Faktor risiko utama stroke meliputi hipertensi, diabetes, merokok, dan gaya hidup sedentari. Deteksi dini terhadap individu dengan risiko tinggi sangat penting untuk mencegah kejadian stroke. Namun, keterbatasan dalam akses layanan kesehatan dan kurangnya kesadaran masyarakat seringkali menghambat upaya pencegahan.​

Dalam konteks ini, pemanfaatan teknologi dan data science menjadi sangat penting. Dengan memanfaatkan data historis pasien dan teknik machine learning, kita dapat membangun model prediktif yang mampu mengidentifikasi individu yang memiliki risiko tinggi terkena stroke. Model semacam ini sangat bermanfaat untuk digunakan oleh tenaga medis, instansi kesehatan, hingga masyarakat umum dalam rangka mendukung pengambilan keputusan preventif yang cepat dan akurat.​


## Business Understanding

Pada bagian ini, akan menjelaskan mengenai proses klarifikasi masalah yang terdiri dari _Problem Statement_, _Goals_ dan _Solution Statements_.

### Problem Statements

Bagaimana mengidentifikasi pasien dengan risiko tinggi terhadap stroke sebelum gejala serius muncul.

### Goals

Tujuan dari proyek ini adalah untuk mengidentifikasi pasien dengan risiko tinggi terhadap stroke sebelum gejala serius muncul dengan membangun model klasifikasi yang mampu memprediksi apakah seseorang termasuk dalam kategori "berisiko stroke" berdasarkan informasi demografis yang ada.

### Solution statements

Solusi yang diusulkan adalah membangun dan membandingkan beberapa model klasifikasi seperti K-Nearest Neighbors (KNN), Random Forest, dan AdaBoost untuk memprediksi risiko stroke. 
Untuk mengukur kinerja dari model yang dibangun, digunakan metrik evaluasi klasifikasi, yaitu:
- Akurasi (Accuracy)
- Precision
- Recall (Sensitivity)
- F1-Score

## Data Understanding
Data yang digunakan dalam proyek ini adalah **35000** data **Stroke Risk Prediction Dataset based on Literature** yang dapat diunduh dari situs [Kaggle](https://www.kaggle.com/datasets/mahatiratusher/stroke-risk-prediction-dataset-v2). Terdapat 19 fitur (kolom) yang terdapat pada dataset ini.

### Variabel-variabel pada Stroke Risk Prediction Dataset based on Literature dataset adalah sebagai berikut:

1. Chest Pain	
- Binary (0/1): Menunjukkan apakah individu mengalami nyeri dada, gejala umum kondisi kardiovaskular.

2. Shortness of Breath	
- Binary (0/1): Menunjukkan apakah orang tersebut mengalami kesulitan bernapas, yang mungkin mengindikasikan masalah jantung atau paru-paru.

3. Irregular Heartbeat	
- Binary (0/1): Menunjukkan apakah orang tersebut memiliki detak jantung tidak teratur, faktor risiko stroke yang potensial.

4. Fatigue & Weakness	
- Binary (0/1): Menunjukkan kelelahan terus-menerus dan kelemahan otot, tanda-tanda umum masalah kardiovaskular.

5. Dizziness	
- Binary (0/1): Melaporkan apakah individu tersebut sering mengalami pusing, yang mungkin terkait dengan sirkulasi yang buruk.

6. Swelling (Edema)	
- Binary (0/1): Menunjukkan pembengkakan pada ekstremitas karena retensi cairan, masalah kardiovaskular yang potensial.

7. Neck/Jaw/Pain	
- Binary (0/1): Menjelaskan nyeri di area ini, yang dapat menjadi tanda peringatan stroke atau serangan jantung.

8. Excessive Sweating	
- Binary (0/1): Menunjukkan apakah individu mengalami keringat yang tidak biasa, yang dapat mengindikasikan gangguan kardiovaskular.

9. Persistent Cough	
- Binary (0/1): Menunjukkan batuk kronis, yang dapat dikaitkan dengan gagal jantung.

10. Nausea/Vomiting	
- Binary (0/1): Melaporkan mual atau muntah yang sering, yang dapat dikaitkan dengan kejadian kardiovaskular.

11. High Blood Pressure	
- Binary (0/1): Mewakili apakah orang tersebut memiliki tekanan darah tinggi, faktor risiko utama untuk stroke.

12. Chest Discomfort (Activity)	
- Binary (0/1): Menunjukkan apakah individu mengalami ketidaknyamanan dada selama aktivitas fisik.

13. Cold Hands/Feet	
- Binary (0/1): Menunjukkan apakah orang tersebut sering mengalami ekstremitas dingin, yang merupakan tanda kemungkinan masalah sirkulasi.

14. Snoring/Sleep Apnea	
- Binary (0/1): Melaporkan apakah orang tersebut mengalami apnea tidur, yang dapat meningkatkan risiko stroke.

15. Anxiety/Feeling of Doom	
- Binary (0/1): Menunjukkan apakah orang tersebut sering mengalami kecemasan atau perasaan akan datangnya malapetaka, yang dapat dikaitkan dengan gangguan kardiovaskular.

16. Stroke Risk Percentage
- Continuous (0-100%): Perkiraan persentase risiko terkena stroke, berdasarkan tingkat keparahan gejala dan indikator medis.

17. At Risk (Binary)	
- Binary (0/1): Menunjukkan apakah orang tersebut diklasifikasikan sebagai berisiko terkena stroke (1) atau tidak (0).

18. Age	
- Integer: Usia individu, faktor penting dalam menilai risiko stroke.

19. Gender
- String: Male/Female

### Explanatory Data Analysis

1. Distribusi Stroke Risk
(https://github.com/fabasassa-lab/Stroke-Risk-Prediction/blob/main/image/risk.png?raw=true)

2. Distribusi Usia
(https://github.com/fabasassa-lab/Stroke-Risk-Prediction/blob/main/image/age_distribution.png?raw=true)

3. Distribusi Gender vs Risk
(https://github.com/fabasassa-lab/Stroke-Risk-Prediction/blob/main/image/gender_risk.png?raw=true)

4. Confussion Matrix
(https://github.com/fabasassa-lab/Stroke-Risk-Prediction/blob/main/image/cm_analysis.png?raw=true)

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

_Referensi:_
[1] Venketasubramanian, N., Yudiarto, F. L., & Tugasworo, D. (2022). Stroke burden and stroke services in Indonesia. Frontiers in Neurology, 13, 850282. https://doi.org/10.3389/fneur.2022.850282

[2] Mahatir Ahmed Tusher, "Stroke Risk Prediction Dataset based on Literature", Kaggle, https://www.kaggle.com/datasets/mahatiratusher/stroke-risk-prediction-dataset-v2
