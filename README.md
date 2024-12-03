# CapstoneProject3PutraHardi-Hotel-Booking-Demand
Data Analysis and Model Development for Hotel Booking Demand Dataset


## 1. Business Problem Understanding
Context

Dataset ini berisi informasi pemesanan untuk sebuah hotel yang berlokasi di Portugal. Informasi ini mencakup berbagai aspek seperti negara asal pelanggan, tipe reservasi, jumlah pembatalan sebelumnya, hingga permintaan khusus. Semua informasi pribadi telah dihapus untuk menjaga kerahasiaan data.

Hotel menghadapi tantangan dalam memahami pola perilaku pelanggan untuk meningkatkan pengelolaan reservasi dan pengalaman pelanggan. Dengan adanya dataset ini, kita dapat menggali pola-pola tersebut untuk memberikan wawasan yang dapat membantu meningkatkan efisiensi dan kualitas layanan hotel.

Problem Statement

Salah satu tantangan utama dalam industri perhotelan adalah memprediksi perilaku pelanggan terkait pembatalan, kebutuhan khusus, dan perubahan dalam reservasi. Memahami faktor-faktor yang memengaruhi hal tersebut sangat penting untuk meningkatkan kepuasan pelanggan, mengoptimalkan tingkat hunian hotel, serta mengurangi kerugian akibat pembatalan mendadak.

Goals

Tujuan dari analisis ini adalah:

Memahami pola pembatalan pemesanan: Mengidentifikasi faktor-faktor yang paling berpengaruh terhadap pembatalan.
Menganalisis permintaan pelanggan: Mengetahui pola terkait kebutuhan seperti ruang parkir atau permintaan khusus lainnya.
Memberikan wawasan strategis: Menghasilkan rekomendasi untuk meningkatkan pengelolaan reservasi, memaksimalkan tingkat hunian, dan mengurangi potensi kerugian akibat pembatalan.
Analytic Approach

Langkah-langkah analisis yang akan dilakukan meliputi:

Eksplorasi data untuk memahami distribusi dan pola dari masing-masing fitur.
Identifikasi korelasi antara variabel, terutama yang berhubungan dengan pembatalan dan permintaan pelanggan.
Membangun model prediktif untuk memprediksi kemungkinan pembatalan pemesanan.
Interpretasi hasil analisis dan penyusunan rekomendasi berbasis data.
Metric Evaluation

Metode evaluasi yang digunakan adalah:

Accuracy, Precision, dan Recall
Accuracy: Mengukur seberapa tepat model dalam mengklasifikasikan data.
Precision: Mengetahui seberapa relevan prediksi pembatalan.
Recall: Mengetahui seberapa banyak kasus pembatalan yang teridentifikasi dengan benar.
F1-Score Kombinasi rata-rata harmonis antara Precision dan Recall untuk memberikan keseimbangan evaluasi.
Confusion Matrix Menampilkan jumlah prediksi benar (True Positive dan True Negative) serta salah (False Positive dan False Negative).

## 2. Data Understanding
Dataset ini terdiri dari 83.573 baris dan 11 kolom. Setiap baris merepresentasikan informasi terkait satu pemesanan, dengan berbagai atribut yang menjelaskan detail pemesanan seperti asal pelanggan, tipe reservasi, dan status pembatalan. Berikut adalah cuplikan data:

Attributes Information

Attribute	Data Type	Description
country	Object	Negara asal pelanggan.
market_segment	Object	Penunjukan segmen pasar.
previous_cancellations	Integer	Jumlah pemesanan sebelumnya yang dibatalkan oleh pelanggan sebelum pemesanan saat ini.
booking_changes	Integer	Jumlah perubahan yang dilakukan pada pemesanan sejak dimasukkan hingga saat check-in/batal.
deposit_type	Object	Indikasi apakah pelanggan melakukan deposit untuk menjamin pemesanan.
days_in_waiting_list	Integer	Jumlah hari pemesanan berada dalam daftar tunggu sebelum dikonfirmasi kepada pelanggan.
customer_type	Object	Tipe pemesanan (misalnya: Transient, Contract, Transient-Party).
reserved_room_type	Object	Kode jenis kamar yang dipesan. Kode digunakan untuk menjaga kerahasiaan.
required_car_parking_spaces	Integer	Jumlah ruang parkir mobil yang dibutuhkan oleh pelanggan.
total_of_special_requests	Integer	Jumlah permintaan khusus yang diajukan oleh pelanggan (misalnya: tempat tidur twin atau lantai tinggi).
is_canceled	Integer	Nilai yang menunjukkan apakah pemesanan dibatalkan (1) atau tidak (0).


## 3. Data Modelling
 Model yang digunakan adalah Random Forest Classifier dengan dan tanpa SMOTE (Synthetic Minority Oversampling Technique) dan Hyperparameter Tuning


## 4. Analisis dan Rekomendasi
Analisis

Model: Random Forest digunakan untuk memprediksi pembatalan hotel.
Precision dan Recall menunjukkan hasil yang baik, dengan kemampuan model untuk mengidentifikasi pembatalan dan mengurangi kesalahan prediksi. Terdapat dampak positif dan negative dari penggunaan SMOTE dan Hyperparamter Tuning pada Model
Model sudah cukup stabil, namun dapat lebih ditingkatkan dengan fitur tambahan atau model lain.

Rekomendasi Bisnis

Peningkatan Akurasi: Pertimbangkan untuk mengumpulkan lebih banyak data terkait pelanggan untuk meningkatkan akurasi prediksi pembatalan.
Model Alternatif: Eksplorasi model lain (misalnya, XGBoost atau Gradient Boosting) untuk kemungkinan peningkatan performa.
Optimasi Pengelolaan Pembatalan: Gunakan prediksi pembatalan untuk meningkatkan manajemen sumber daya dan pengelolaan permintaan.
Tindakan Preventif: Terapkan strategi untuk mengurangi pembatalan berdasarkan prediksi, seperti penawaran khusus bagi pelanggan yang lebih mungkin untuk membatalkan.

