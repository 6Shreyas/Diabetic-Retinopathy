SA-EViT: Spatial Attention-based Efficient Vision Transformer for Diabetic Retinopathy Classification

Overview
This repository contains the implementation of **SA-EViT**, a hybrid deep learning model for **Diabetic Retinopathy (DR) classification** using retinal fundus images.

The proposed model integrates:
- **EfficientNet-B0** for strong local feature extraction  
- A novel **Spatial Attention Module (SAM)** to capture multi-scale spatial features  
- A lightweight **Vision Transformer (ViT)** to learn global contextual representations  

Unlike conventional ViTs, this model is designed to be **computationally efficient** while maintaining high accuracy, making it suitable for real-world medical applications.

---

## Key Contributions
-  Proposed a **hybrid CNN–ViT architecture** combining local and global feature learning  
-  Designed a **novel Spatial Attention Module (SAM)** with parallel pooling and dilated convolutions  
-  Developed a **lightweight ViT encoder** with significantly fewer parameters  
-  Addressed **class imbalance** and multi-scale feature challenges in DR datasets  
-  Performed detailed **ablation studies** to validate each component  
-  Compared performance with multiple **state-of-the-art (SOTA) models**

---

## Model Architecture
The SA-EViT architecture consists of:

1. **EfficientNet-B0 Backbone**
   - Extracts rich local features from retinal images  

2. **Parallel SAM + ViT Branch**
   - SAM enhances spatial attention using pooling + dilated convolutions  
   - ViT processes feature maps into patches to capture global dependencies  

3. **Feature Fusion**
   - Outputs from CNN and ViT branches are concatenated  
   - Final classification is performed using a softmax layer  

This hybrid design enables the model to learn both **fine-grained lesions** and **global retinal structures** effectively.

---

##  Results
The proposed model was evaluated on two benchmark datasets:

# APTOS 2019
- Accuracy: **84.0%**
- F1-Score: **0.84**

# EyePACS
- Accuracy: **80.2%**
- F1-Score: **0.756**

The model outperforms several SOTA models such as:
- Vanilla ViT  
- EfficientNet-B0  
- MobileNetV2  
- ConvNext-V2  

while maintaining lower computational complexity.

---
