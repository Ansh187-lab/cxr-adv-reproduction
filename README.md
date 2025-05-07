

# Reproducing "An Adversarial Approach for the Robust Classification of Pneumonia from Chest Radiographs"

This repository contains code and documentation for reproducing the results from the paper:

"An Adversarial Approach for the Robust Classification of Pneumonia from Chest Radiographs" (2019)**  
[Link to Paper](https://arxiv.org/abs/2001.04051)

---

## 📌 Project Summary

This reproduction was conducted as part of the DL4H Spring 2025 course at the University of Illinois. The goal was to replicate the paper’s adversarial training method on the NIH ChestX-ray14 dataset using a DenseNet121 backbone.

---

## 🖼️ Dataset

- **NIH ChestX-ray14** (subset of 1,000–2,000 images for training/evaluation)
- Preprocessed to size 224×224
- Images stored in `/data/images-224/`
- Labels from `nih_metadata.csv`

---

## 🛠️ Setup & Requirements

- Python 3.11
- PyTorch ≥ 2.0
- Torchvision
- NumPy, Pandas, scikit-learn, tqdm, matplotlib

```bash
pip install -r requirements.txt

# Clone the repo
git clone https://github.com/Ansh187-lab/cxr-adv-reproduction.git
cd cxr_adv

# Train the standard model
python train.py NIH Standard

# Train the adversarial model
python train.py NIH Adversarial

