# uas-deep-learning-brain-tumor
UAS Deep Learning: Brain Tumor MRI Classification using CNN and Transfer Learning
# Brain Tumor MRI Classification using Deep Learning

## Identitas Kelompok
- Mata Kuliah : Deep Learning  
- Program Studi : Teknik Informatika  
- Semester : 7
- Kelas : 7a 
- Dosen Pengampu : Asriyanik, M.T.  
- Disusun Oleh :
  Tanaya Salsabila Arliansyah (2230511040 )
  Rani Febriani (2230511012)  
  M. Arya Krismawan (2230511016) 
  Gerie Panca Sukma (2230511018)
  Ghani Edytia Oktaviansyah (2230511006) 

## Latar Belakang dan Tujuan
Tumor otak merupakan salah satu penyakit serius yang membutuhkan diagnosis akurat.
Pemanfaatan Deep Learning, khususnya Convolutional Neural Network (CNN), dapat membantu
mengklasifikasikan citra MRI otak secara otomatis untuk mendukung proses diagnosis.

Tujuan dari proyek ini adalah membangun model Deep Learning berbasis CNN dengan pendekatan
Transfer Learning untuk mengklasifikasikan citra MRI otak ke dalam empat kelas, yaitu:
glioma, meningioma, notumor, dan pituitary.

## Deskripsi Dataset
Dataset yang digunakan adalah **Brain Tumor MRI Dataset** yang diperoleh dari Kaggle:

https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

Dataset terdiri dari:
- 4 kelas: glioma, meningioma, notumor, pituitary
- Data citra MRI grayscale
- Pembagian data:
  - Training
  - Validation
  - Testing

Dataset **tidak diunggah ke GitHub** karena berukuran besar, hanya disertakan link sumber.

## Metodologi dan Arsitektur Model
Metode yang digunakan adalah **Transfer Learning** dengan arsitektur **EfficientNetB0**
yang telah dilatih sebelumnya menggunakan dataset ImageNet.

Tahapan utama:
1. Preprocessing data (resize, normalisasi)
2. Data augmentation (flip, rotation, zoom)
3. Training CNN dengan base model dibekukan
4. Fine-tuning dengan membuka sebagian layer akhir
5. Evaluasi model menggunakan data testing

## Hasil dan Evaluasi
Evaluasi dilakukan menggunakan:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Hasil evaluasi menunjukkan bahwa model mampu mengenali pola citra MRI,
meskipun masih terdapat ketidakseimbangan performa antar kelas.

## Analisis dan Pembahasan
Model menunjukkan indikasi overfitting ringan,
di mana akurasi training lebih tinggi dibandingkan akurasi testing.
Hal ini disebabkan oleh keterbatasan jumlah data dan kompleksitas citra MRI.

## Kesimpulan
Model CNN berbasis Transfer Learning berhasil dibangun dan diuji
untuk klasifikasi tumor otak berbasis citra MRI.
Meskipun akurasi belum optimal, pendekatan ini menunjukkan potensi
yang baik untuk pengembangan sistem pendukung diagnosis medis.  
- TensorFlow & Keras Documentation  
- EfficientNet: Rethinking Model Scaling for CNNs
