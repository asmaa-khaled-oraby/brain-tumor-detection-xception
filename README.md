## Brain Tumor Classification using Xception CNN

A deep learning project that classifies brain MRI scans into 4 categories: **Glioma**, **Meningioma**, **Pituitary Tumor**, and **No Tumor**.

---

## Pre-trained Model

The model used is **Xception** (Extreme Inception), pre-trained on ImageNet. Xception uses depthwise separable convolutions which makes it more efficient and accurate than traditional CNNs. The original classification head was removed and replaced with a custom head designed for this 4-class problem.

---

## Dataset

**Brain Tumor MRI Dataset** by Masoud Nickparvar

🔗 https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

- Total images: 7,023 MRI scans
- Classes: Glioma, Meningioma, No Tumor, Pituitary
- Already split into Training and Testing folders
  
---

## Classes

- Glioma
- Meningioma
- No Tumor
- Pituitary Tumor

---


## Fine-Tuning Strategy

Training was done in two phases to get the best results without damaging the pretrained weights:

**Phase 1** — The Xception base was fully frozen and only the new classification head was trained. This lets the new layers learn first before touching the pretrained weights. Learning rate: 1e-3

**Phase 2** — The last convolutional block of Xception (block14) was unfrozen and fine-tuned along with the head. This allows the model to adapt its high-level features to brain MRI images specifically. Learning rate: 1e-5

---

## Results

| Metric | Value |
|--------|-------|
| Training Accuracy | ~93% |
| Validation Accuracy | ~89% |
| Number of Classes | 4 |
| Input Image Size | 299 × 299 |
