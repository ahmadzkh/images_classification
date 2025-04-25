# 📊 Proyek Klasifikasi Gambar: Burung vs Drone

> **Nama**: Ahmad Zaky Humami  
> **Email**: mc009d5y0493@student.devacademy.id  
> **ID Dicoding**: MC009D5Y0493  

## 🧠 Deskripsi Proyek

Proyek ini bertujuan untuk mengembangkan model deep learning menggunakan Convolutional Neural Network (CNN) untuk mengklasifikasikan gambar antara dua kelas: **burung** dan **drone**. Model dikembangkan menggunakan TensorFlow dan Keras, serta memenuhi kriteria struktur dataset, preprocessing, augmentasi data, evaluasi model, dan konversi model ke berbagai format seperti SavedModel, TFLite, dan TFJS.

## 📁 Struktur Direktori

```
  Proyek Akhir Klasifikasi Gambar/
  ├─── tfjs_model
  | ├─── group1-shard1of1.bin
  | └─── model.json
  ├─── tflite
  | ├─── model.tflite
  | └─── label.txt
  ├─── saved_model
  | ├─── saved_model.pb
  | └─── variables
  ├─── [Image Classification]_Ahmad Zaky Humami.ipynb
  ├─── README.md
  └─── requirements.txt
```

## 📦 Informasi Dataset

  Dataset yang digunakan berasal dari Kaggle:  
  🔗 [Bird vs Drone Dataset by stealthknight](https://www.kaggle.com/datasets/stealthknight/bird-vs-drone)
  
  - Ukuran: ±1.18 GB
  - Jumlah gambar: ±21,000 gambar untuk masing-masing label (.jpg dan .txt)
  - Terdiri atas tiga subset: `train`, `valid`, dan `test`
  - Format anotasi: YOLO-style (dalam `.txt`)
  
  Struktur Direktori Dataset:
```  
  Dataset/
  ├─── test/
  | ├─── images/
  | └─── labels/
  ├─── train/
  | ├─── images/
  | └─── labels/
  └─── valid/
    ├─── images/
    └─── labels/
```

---

# 🚀 Instalasi dan Menjalankan Aplikasi
## 1️⃣ Clone Repository
```bash
  git clone https://github.com/ahmadzkh/images_classification
  cd images_classification
```

## 2️⃣ Install Environment
Setelah itu, instal streamlit dan semua dependensi dari file `requirements.txt` dengan perintah:
```bash
  pip install -r requirements.txt
```

## 3️⃣ Siapkan API Key Kaggle
Letakkan file kaggle.json Anda di root folder proyek. Lalu jalankan:
```python
  import os, shutil

  os.makedirs(os.path.expanduser("~/.kaggle"), exist_ok=True)
  shutil.copy("kaggle.json", os.path.expanduser("~/.kaggle/kaggle.json"))
  os.chmod(os.path.expanduser("~/.kaggle/kaggle.json"), 0o600)
```

---

# 🏗️ Arsitektur Model
  Model CNN dibangun menggunakan Sequential API dengan beberapa layer:
  - Conv2D + MaxPooling2D
  - Flatten + Dense
  - Dropout
  - Binary Output
  
  Dilengkapi dengan:
  - EarlyStopping
  - ModelCheckpoint

---

# 📈 Hasil Evaluasi
- Akurasi Training: ±...%
- Akurasi Validation: ±...%
- Model terbaik disimpan dalam best_model.h5

# 🧪 Format Model Output
Model dikonversi ke tiga format:
  - SavedModel
  - TensorFlow Lite (TFLite)
  - TensorFlow.js (TFJS)

# 📧 Kontak
Jika Anda memiliki pertanyaan atau masukan, silakan hubungi:
📩 Email: mc009d5y0493@student.devacademy.id
🧑‍💻 Dicoding ID: MC009D5Y0493

> Belajar Pengembangan Machine Learning - Ahmad Zaky Humami MC009D5Y0493

© 2025 Ahmad Zaky Humami — All Rights Reserved.
