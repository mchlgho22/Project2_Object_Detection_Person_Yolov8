# 🚀 YOLOv8 Person Detection (COCO Dataset)

## 📌 Overview

Project ini bertujuan untuk membangun model **Object Detection (Person Detection)** menggunakan **YOLOv8** dengan dataset dari COCO 2017.

Model dilatih untuk mendeteksi objek **manusia (person)** dengan performa yang cukup baik menggunakan subset dataset.

---

## 🧠 Model & Tools

* YOLOv8 (Ultralytics)
* Python
* Google Colab (GPU Tesla T4)
* COCO Dataset 2017
* OpenCV, Matplotlib

---

## 📂 Dataset

Dataset berasal dari COCO 2017:

* train2017
* val2017
* annotations

### 🔍 Data Preparation

* Filter hanya class: **person**
* Total data digunakan: **5000 images**

  * Train: 4000 images (80%)
  * Validation: 1000 images (20%)

---

## ⚙️ Pipeline Project

### 1. Mount Google Drive

Digunakan untuk menyimpan dataset & model.

### 2. Install Dependencies

```bash
pip install ultralytics pycocotools tqdm
```

### 3. Download & Extract COCO Dataset

### 4. Data Preprocessing

* Filtering class *person*
* Convert format:

  * COCO → YOLO format
* Split dataset (train & validation)

### 5. Training Model

Model yang digunakan:

```python
YOLO("yolov8m.pt")
```

Parameter training:

* Epochs: 10
* Image size: 640
* Batch size: 16
* Optimizer: SGD / Auto 
---

## 📊 Hasil Training

| Metric    | Value |
| --------- | ----- |
| mAP50     | 0.686 |
| mAP50-95  | 0.426 |
| Precision | 0.777 |
| Recall    | 0.583 |

---

## 📈 Visualisasi

### 🔹 Training Results

* Loss curve
* mAP curve

### 🔹 Confusion Matrix

Menunjukkan performa klasifikasi model

### 🔹 Ground Truth vs Prediction

* Kotak hijau → Ground Truth
* Kotak biru → Prediksi model

---

## 🧪 Testing

### 🖼️ Image Testing

* Upload gambar
* Model akan:

  * Deteksi person
  * Menampilkan bounding box + confidence score

### 🎥 Video Testing

* Upload video
* Output:

  * Video dengan bounding box deteksi
  * Disimpan ke Google Drive

---

## 📦 Output Project

File penting yang disimpan:

```
model/
├── best.pt
├── last.pt
├── results.png
├── results.csv
├── confusion_matrix.png
```

---

## 📐 Evaluation Metrics

* **IoU (Intersection over Union)**
* **Precision**
* **Recall**
* **mAP (mean Average Precision)**

---

## 💡 Insight

* Model cukup stabil untuk deteksi person
* Augmentasi membantu meningkatkan generalisasi
* Dataset subset (5000 images) sudah cukup untuk performa baik

---

## ⚠️ Catatan

* Training dilakukan di Google Colab (GPU terbatas)
* Dataset besar → sebaiknya simpan di Google Drive
* Clear output sebelum upload ke GitHub agar file tidak terlalu besar

---

## 👨‍💻 Author

Michael Salabintago

---

## ⭐️ Support

Jika project ini membantu, jangan lupa ⭐️ repository ini!
