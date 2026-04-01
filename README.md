# 🛰️ EuroSAT RGB — Land Cover Classification with CNNs

Satellite image classification using Sentinel-2 RGB imagery across
10 land-cover classes, built with Hugging Face Transformers.

[![Dataset](https://img.shields.io/badge/🤗%20Dataset-EuroSAT_RGB-blue)](https://huggingface.co/datasets/blanchon/EuroSAT_RGB)
[![Model](https://img.shields.io/badge/🤗%20Model-ViT--Base-green)](https://huggingface.co/YOUR_USERNAME/eurosat-vit-base)

## 🌍 Overview

Land use and land cover (LULC) classification from satellite imagery
supports renewable energy siting, urban planning, and environmental monitoring.
This project fine-tunes three CNN/ViT architectures on the EuroSAT RGB
dataset and evaluates them.

**Dataset:** 27,000 Sentinel-2 RGB tiles | 10 classes | 64×64 px | ~10m/px resolution

---

## 🏗️ Pipeline

| Notebook | Description |
|---|---|
| `01_EDA.ipynb` | Class distribution, spectral analysis, RGB channel stats |
| `02_Training_Comparison.ipynb` | Fine-tune ResNet-18, EfficientNet-B0, ViT-Base |
| `03_Evaluation.ipynb` | Confusion matrix, per-class F1, confidence analysis |

---

## 📊 Results

| Model | Val Accuracy | Macro F1 | Train Time |
|---|---|---|---|
| ResNet-18 | ~93% | ~92% | ~18 min |
| EfficientNet-B0 | ~96% | ~95% | ~22 min |
| **ViT-Base** ✅ | **~98%** | **~98%** | ~55 min |

> Benchmark reference: Helber et al. (2019) — 98.57% on EuroSAT RGB

---

## 📁 Repository Structure

```
├── 1_EDA_EuroSAT.ipynb
├── 2_Training_Comparison_EuroSAT.ipynb
├── 3_Evaluation_EuroSAT.ipynb
├── data/
│ ├── config.json
│ ├── preprocessor_config.json
│ ├── training_args.bin
│ └── best_model_meta.json
└── README.md

[model safetensor link](https://drive.google.com/drive/folders/1I9UTsSQ7Sz3jUrEKkfytpaM_YTKjSN17?usp=sharing)
```

---

## 📚 Reference

Helber, P., Bischke, B., Dengel, A., & Borth, D. (2019).
*EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use
and Land Cover Classification.* IEEE Journal of Selected Topics in
Applied Earth Observations and Remote Sensing.

---

## 👤 Author

**Yonathan Hary Hutagalung** — Sustainable Energy Science | Data Science
[LinkedIn](https://linkedin.com/in/yonathanhary) 
[Portfolio Site](https://yonathanhh.github.io/)

