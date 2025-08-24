# SMSAT-Time-Series-Acoustic-Data
## 🩺 Project Overview

This work contributes a validated multimodal dataset and a scalable deep learning framework for affective computing applications in stress monitoring, mental well-being, and therapeutic audio-based interventions

The study is based on a **custom heart rate time series dataset** captured from real-world acoustic recordings, with preprocessing and exploratory analysis included.

![Alt Text](SMSAT_Gihub.jpg)
---

## 🔍 Dataset

A custom dataset of heart rate time series captured as acoustic signals. It includes **normal**, **abnormal**, and **borderline** cases, with accompanying metadata for classification purposes.

- 📁 **Dataset Access**: 
🔗 [https://www.kaggle.com/datasets/crdkhan/qmsat-dataset/data](https://www.kaggle.com/datasets/crdkhan/qmsat-dataset/data) 
- 📈 **Raw Data Analysis Notebook**:  
🔗 [https://www.kaggle.com/code/crdkhan/1-dataset-rawaudioanalysis](https://www.kaggle.com/code/crdkhan/1-dataset-rawaudioanalysis)

---


## 📁 Repository Contents

| File/Notebook | Description |
|---------------|-------------|
| `1-dataset-rawaudioanalysis.ipynb` | Preprocesses raw acoustic data and extracts spectrograms and waveform features. |
| `2-dataset-validation.ipynb` | Validates metadata, checks data balance, and visualizes distributions. |
| `3-smsat-encoder-train-cosine-0-9975.ipynb` | Trains a CNN encoder using cosine similarity-based contrastive loss. |
| `4-calmanalysismodel-cam-acc-0-99.ipynb` | CAM-based model with attention for stress classification. |
| `4multiclass-binary-otherbasemodels-ablation-study.ipynb` | Baseline comparison for binary and multi-class classification models. |
| `5-anova-paiwise-t-test.ipynb` | Statistical significance testing (ANOVA, t-test) on model results. |
| `6-calmanalysismodel-cam.ipynb` | Final CAM-based model and evaluation. |
| `7-modelvisulization.ipynb` | Visualizes CAM attention maps and classification results. |
| `README.md` | Project instructions and overview. |
| `SMSAT_Gihub.jpg` | Illustrative dataset image. |

---



---

## 📄 License

This repository will be licensed under the **MIT License** upon release.

---

## ✉️ Contact

For collaboration or questions, please reach out via:  
📧 **engineersuleman118@gmail.com**

---
---

## 🧩 Methods & Classes Reference

This project defines core classes and helper methods inside Jupyter notebooks.  
Here’s a quick reference of what you’ll find:

### 📂 Dataset & Preprocessing
- **`QMSAT` / `RawAudioDataset`**  
  PyTorch dataset wrappers for heart sound recordings.  
  - `__init__(root_dir, sample_rate, transform=None)`  
  - `__getitem__(idx)` → waveform & label  
  - `__len__()` → dataset size  

- **Feature Extraction Functions**  
  - `compute_amplitude_envelope(waveform)`  
  - `extract_mfcc_features(waveform, sr, n_mfcc)`  
  - `extract_time_features(waveform)`  
  - `extract_wavelet_features(waveform)`  

---

### 🎛️ Data Augmentation
- **`AudioAugmentations`**  
  Creates multiple “views” of an audio signal for self-supervised learning.  
  - `add_noise(waveform)`  
  - `time_stretch(waveform)`  
  - `pitch_shift_fn(waveform)`  
  - `apply_spec_augment(waveform)`  
  - `random_crop(waveform)`  
  - `__call__(waveform)` → augmented version  

---

### 🧠 Self-Supervised Encoder
- **`QSMATATSEncoder`** (1D CNN encoder with projection head)  
  - `forward(x)` → projection for training  
  - `encode(x)` → embeddings for downstream tasks  

- **Training Helpers**  
  - `train_self_supervised(model, loader, ...)`  
  - `extract_audio_labels(batch)`  
  - `plot_loss_curves(...)`, `plot_cosine_curves(...)`  
  - `compute_and_plot_statistics(model, dataloader, method)`  

---

### 🎯 Calmness Analysis
- **`CalmnessAnalysisModel`**  
  Simple feed-forward classifier for calmness prediction.  
  - `__init__(input_dim, hidden_dim, num_classes)`  
  - `forward(audio_features)` → logits  

- **Visualization Tools**  
  - Grad-CAM style heatmaps for model interpretability  

---

### 📊 Statistics
- **ANOVA & t-tests**  
  - Pairwise comparisons between feature sets  
  - Confirms significance of ablation studies  

---

### 📈 Visualization
- **EDA Plots** → amplitude envelopes, spectrograms  
- **Embeddings** → PCA/TSNE of latent spaces  
- **CAM Overlays** → interpret calmness predictions  


## Citation
``` bibtex
@misc{suleman2025smsatmultimodalacousticdataset,
      title={SMSAT: A Multimodal Acoustic Dataset and Deep Contrastive Learning Framework for Affective and Physiological Modeling of Spiritual Meditation}, 
      author={Ahmad Suleman and Yazeed Alkhrijah and Misha Urooj Khan and Hareem Khan and Muhammad Abdullah Husnain Ali Faiz and Mohamad A. Alawad and Zeeshan Kaleem and Guan Gui},
      year={2025},
      eprint={2505.00839},
      archivePrefix={arXiv},
      primaryClass={cs.SD},
      url={https://arxiv.org/abs/2505.00839}, 
}


