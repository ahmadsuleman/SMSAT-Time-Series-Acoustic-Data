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


## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/engineersuleman/SMSAT-Time-Series-Acoustic-Data.git
cd SMSAT-Time-Series-Acoustic-Data
```

### 2. Create Virtual Environment (Always show details)

```bash
python -m venv smsat-env
source smsat-env/bin/activate  # Windows: smsat-env\\Scripts\\activate
```

```bash
python -m venv smsat-env
source smsat-env/bin/activate  # Windows: smsat-env\Scripts\activate
```

### 3. Install Dependencies (Always show details)

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy librosa torch torchvision torchaudio plotly ipywidgets
```

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy librosa torch torchvision torchaudio plotly ipywidgets
```

---

## 🚀 Running the Project

### 🚀 Running the Project

#### Suggested Execution Order:

1. `1-dataset-rawaudioanalysis.ipynb`  
2. `2-dataset-validation.ipynb`  
3. `3-smsat-encoder-train-cosine-0-9975.ipynb`  
4. `4-calmanalysismodel-cam-acc-0-99.ipynb`  
5. `4multiclass-binary-otherbasemodels-ablation-study.ipynb`  
6. `5-anova-paiwise-t-test.ipynb`  
7. `6-calmanalysismodel-cam.ipynb`  
8. `7-modelvisulization.ipynb`  

> ⚠️ Make sure all notebook paths match your directory structure after dataset placement.

---

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


