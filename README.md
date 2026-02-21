Brain Tumor Classification using Xception CNN
A deep learning project that classifies brain MRI scans into 4 categories: Glioma, Meningioma, Pituitary Tumor, and No Tumor.

Pre-trained Model
The model used is Xception (Extreme Inception), pre-trained on ImageNet. Xception uses depthwise separable convolutions which makes it more efficient and accurate than traditional CNNs. The original classification head was removed and replaced with a custom head designed for this 4-class problem.

Dataset
Brain Tumor MRI Dataset by Masoud Nickparvar
🔗 https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

Total images: 7,023 MRI scans
Classes: Glioma, Meningioma, No Tumor, Pituitary
Already split into Training and Testing folders


Accuracy
PhaseAccuracyPhase 1 - Head only~88%Phase 2 - Fine-tuned~93%Validation Accuracy~89%

Classes

Glioma
Meningioma
No Tumor
Pituitary Tumor
