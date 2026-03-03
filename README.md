# 🏠 Image-Based Classification of Indonesian Traditional Houses

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://python.org)
[![FastAI](https://img.shields.io/badge/FastAI-2.x-00A98F)](https://docs.fast.ai)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Deep Learning image classification model to identify **5 types of Indonesian traditional houses** using transfer learning with **ResNet-50** and the **FastAI** framework.

<div align="center">

| Balinese | Batak | Dayak | Javanese | Minangkabau |
|:--------:|:-----:|:-----:|:--------:|:-----------:|
| ![](https://via.placeholder.com/100x80?text=Balinese) | ![](https://via.placeholder.com/100x80?text=Batak) | ![](https://via.placeholder.com/100x80?text=Dayak) | ![](https://via.placeholder.com/100x80?text=Javanese) | ![](https://via.placeholder.com/100x80?text=Minangkabau) |

</div>

---

## ⚠️ Important: Dataset Disclaimer

> **Dataset ini berukuran sangat besar (~4 GB)** dan **tidak di-include dalam repository ini**.
>
> GitHub memiliki batas ukuran file 100 MB dan merekomendasikan ukuran repository di bawah 1 GB. Menyertakan dataset secara langsung akan menyebabkan masalah:
> - Push/pull yang sangat lambat
> - Repository tidak dapat di-clone dengan efisien
> - Potensi penolakan oleh GitHub
>
> **Solusi:** Dataset harus diunduh secara terpisah. Lihat bagian [Dataset Setup](#-dataset-setup) di bawah.

---

## 📋 Project Overview

### Objective
Mengklasifikasikan gambar rumah adat Indonesia ke dalam 5 kategori etnis menggunakan pendekatan deep learning transfer learning.

### Model Architecture
- **Backbone:** ResNet-50 (pretrained on ImageNet)
- **Strategy:** 2-stage transfer learning
  - Stage 1: Train head layers (20 epochs, LR: 1e-4 → 1e-3)
  - Stage 2: Fine-tune full network (10 epochs, LR: 1e-5 → 1e-4)
- **Input size:** 320 × 320 pixels
- **Augmentation:** FastAI standard transforms (flip, rotate, zoom, warp, lighting)

### Classes

| # | Class | Train Images | Description |
|---|-------|:------------:|-------------|
| 1 | **Balinese** | 776 | Rumah adat Bali |
| 2 | **Minangkabau** | 563 | Rumah Gadang, Sumatera Barat |
| 3 | **Javanese** | 249 | Joglo, Jawa |
| 4 | **Batak** | 95 | Rumah Bolon, Sumatera Utara |
| 5 | **Dayak** | 69 | Rumah Betang, Kalimantan |

**Total:** 1,752 training images + 444 test images

---

## 🗂️ Dataset Setup

### Option 1: Download from Kaggle

Dataset tersedia di Kaggle. Download dan extract ke dalam folder project:

```bash
# Menggunakan Kaggle CLI
kaggle datasets download -d <dataset-slug>
unzip <dataset>.zip -d "Indonesian Traditional Houses Dataset"
```

### Option 2: Manual Download

1. Download dataset dari sumber asli
2. Extract ke dalam folder project dengan struktur berikut:

### Expected Directory Structure

```
Image-Based Classification of Indonesian Traditional Houses/
├── 📓 traditional-house-classification-use-fastai.ipynb
├── 📄 README.md
├── 📄 requirements.txt
├── 📄 LICENSE
├── 📄 .gitignore
├── 📁 models/                          ← (generated after training)
│   ├── export.pkl
│   └── stage-final.pth
├── 📄 predictions.csv                  ← (generated after inference)
└── 📁 Indonesian Traditional Houses Dataset/   ← ⚠️ NOT in repo
    ├── 📁 Train/
    │   └── 📁 Train/
    │       ├── 📁 balinese/       (776 images)
    │       ├── 📁 batak/          (95 images)
    │       ├── 📁 dayak/          (69 images)
    │       ├── 📁 javanese/       (249 images)
    │       └── 📁 minangkabau/    (563 images)
    ├── 📁 Test/
        └── 📁 Test/               (444 images)
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- NVIDIA GPU with CUDA support (recommended)
- ~4 GB disk space for dataset

### Installation

```bash
# 1. Clone repository
git clone https://github.com/<username>/Image-Based-Classification-of-Indonesian-Traditional-Houses.git
cd Image-Based-Classification-of-Indonesian-Traditional-Houses

# 2. Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download & place dataset (see Dataset Setup above)

# 5. Run the notebook
jupyter notebook traditional-house-classification-use-fastai.ipynb
```

---

## 📊 Results

> **Note:** Hasil training akan terlihat setelah menjalankan notebook. Confusion matrix dan top losses tersedia di bagian Evaluation pada notebook.

| Metric | Value |
|--------|-------|
| Architecture | ResNet-50 |
| Total Epochs | 30 (20 + 10) |
| Validation Split | 20% |
| Output | `predictions.csv` |

---

## 📁 Output Files

| File | Description |
|------|-------------|
| `predictions.csv` | Prediksi label untuk 444 test images |
| `models/export.pkl` | Complete model export (architecture + weights + vocab) |
| `models/stage-final.pth` | Final training checkpoint |

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| Language | Python 3.10+ |
| Deep Learning | PyTorch 2.x |
| High-level API | FastAI 2.x |
| Model | ResNet-50 (ImageNet pretrained) |
| Visualization | Matplotlib, Seaborn |
| Data | Pandas, NumPy |
| Image Processing | OpenCV |

---

## 📝 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- [FastAI](https://docs.fast.ai/) — High-level deep learning library
- [PyTorch](https://pytorch.org/) — Deep learning framework
- Dataset creators for providing the Indonesian Traditional Houses Dataset
- Indonesian cultural heritage that inspired this project

---

<div align="center">

**⭐ If you find this project useful, please give it a star! ⭐**

</div>
