# FibroHybridNet: A Deep Learning Framework for Fibroglandular Tissue Classification

![Python](https://img.shields.io/badge/python-3.10-blue.svg)
![Pytorch](https://img.shields.io/badge/pytorch-2.1.2-red.svg)

This repository contains the implementation of **FibroHybridNet**, a hybrid deep learning framework for classifying fibroglandular tissue (FGT) in breast MRI into BI-RADS categories.  
FibroHybridNet integrates **2D CNNs, a Vision Transformer, and a 3D CNN** to capture both local and volumetric features, providing improved classification accuracy compared to individual models.

📄 **Reference:**  
If you use this repository, please cite our paper:  
> Meysam Khalaj *et al.*  
> *FibroHybridNet: A Deep Learning Framework for Fibroglandular Tissue Classification with a Statistically Validated Comparison to the BI-RADS Maximum Rule.*  
> (Preprint / Under Review)

---

## 🚀 Features
- Combines **2D CNNs (MobileNetV2, ResNet26)**, a **Vision Transformer (CaiT-S24)**, and a **3D CNN (DenseNet121)**.  
- Evaluates two assessment strategies:  
  - **Probability Averaging (PA)** – superior performance  
  - **BI-RADS Maximum Rule (BMR)** – baseline comparison  
- First **publicly available dataset** for FGT classification in breast MRI.  
- Supports **Grad-CAM visualizations** for model interpretability.  

---

## 📊 Results

| Model          | Accuracy | Precision | Recall | F1 Score | Kappa |
|----------------|----------|-----------|--------|----------|-------|
| DenseNet121 (3D) | 0.838 | 0.856 | 0.808 | 0.824 | 0.770 |
| MobileNetV2 (2D) | 0.808 | 0.868 | 0.762 | 0.792 | 0.725 |
| ResNet26 (2D)    | 0.808 | 0.830 | 0.760 | 0.783 | 0.725 |
| CaiT-S24 (2D)    | 0.838 | 0.849 | 0.788 | 0.809 | 0.769 |
| **FibroHybridNet (2D+3D)** | **0.869** | **0.905** | **0.832** | **0.857** | **0.813** |

✅ FibroHybridNet achieved **almost perfect agreement (κ = 0.813)** with radiologist consensus.

### Access to Trained Models  
All trained and saved models for this project are available for download on [Google Drive](https://drive.google.com/drive/folders/1DEaj3VEu9O0PAvxRPX7WS8tFFsTdYWJv?usp=sharing).
