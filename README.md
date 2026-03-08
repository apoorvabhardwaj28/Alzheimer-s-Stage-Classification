# Alzheimer-s-Stage-Classification
Explainable multi-modal hybrid deep learning framework for Alzheimer’s disease detection using MRI images and clinical data. Combines CNN, Transformer, and ML models with Grad-CAM++ and SHAP for interpretability. Research accepted and presented at IEEE IC3ECSBHI 2026.

# Explainable Multi-Modal Hybrid Deep Learning Framework for Alzheimer’s Disease Detection

This repository contains the implementation of a research project focused on **Alzheimer’s disease detection and stage classification** using **MRI images and clinical tabular data**.

The proposed framework combines **deep learning, machine learning, and explainable AI techniques** to improve diagnostic accuracy while maintaining model interpretability.

📄 This research work has been **accepted and presented at the IEEE IC3ECSBHI 2026 Conference**.

---

# Research Paper

Title:
Explainable Multi-Modal Hybrid Deep and Machine Learning Framework for Alzheimer’s Detection using MRI and Clinical Data

Conference:
IEEE IC3ECSBHI 2026  
(International Conference on Cognitive Computing in Engineering, Communications, Sciences and Biomedical Health Informatics)

Authors:
Apoorva Bhardwaj, Amita Sharma, Manisha Rajoriya

---

# Project Overview

Alzheimer’s disease is a progressive neurodegenerative disorder that affects memory and cognitive function. Early detection is critical for improving patient care and treatment outcomes.

Traditional diagnostic methods often rely on **single-modality data**, such as MRI imaging or clinical assessments alone.

This research proposes a **multi-modal hybrid framework** that integrates:

• Deep learning models trained on **MRI brain scans**  
• Machine learning models trained on **clinical patient data**  
• Explainable AI techniques to interpret predictions  

The system aims to improve classification accuracy while providing **clinically interpretable results**.

---

# Key Features

• Multi-modal learning using MRI and clinical datasets  
• Hybrid CNN + Transformer deep learning architecture  
• Ensemble machine learning models for clinical data  
• Explainable AI using Grad-CAM++ and SHAP  
• Comparative evaluation of multiple deep learning architectures  
• Hybrid ensemble models for improved prediction accuracy  

---

# Dataset

Two datasets were used in this project.

## MRI Dataset

Source:
Kaggle Alzheimer MRI Dataset

Description:
Structural MRI brain scans categorized into four stages of Alzheimer’s disease:

• No Impairment  
• Very Mild Impairment  
• Mild Impairment  
• Moderate Impairment  

Preprocessing steps included:

• Image resizing  
• Normalization  
• Data augmentation  
• Train-test split (80/20)

Images were resized to:

128×128 for CNN models  
224×224 for Transformer models

---

## Clinical Tabular Dataset

The clinical dataset contained approximately **75,000 patient records**.

Features include:

• Age  
• Gender  
• BMI  
• Cognitive test scores  
• Smoking habits  
• Alcohol consumption  
• Sleep quality  
• Diagnosis labels

Preprocessing included:

• Handling missing values  
• Median and mode imputation  
• Label encoding for categorical variables  
• Standardization using z-score normalization

---

# Methodology

The framework consists of three main components.

---

## 1. MRI-Based Deep Learning Models

Multiple deep learning architectures were trained to extract spatial and contextual features from MRI images.

Models evaluated include:

• EfficientNet-B0  
• MobileNetV2  
• DeiT-Tiny Transformer  
• Swin Transformer  
• Capsule Network (CapsNet)

These models were trained using:

• Adam optimizer  
• Cross entropy loss  
• Mixed precision training

---

## 2. Hybrid CNN–Transformer Model

The proposed hybrid model combines:

• EfficientNet-B0  
• MobileNetV2  
• DeiT-Tiny Transformer

Features extracted from these networks are concatenated and passed through a fusion layer for final classification.

This hybrid approach captures:

• Local spatial features (CNN)  
• Global contextual features (Transformer)

---

## 3. Clinical Machine Learning Models

For structured clinical data, several machine learning algorithms were evaluated:

• Logistic Regression  
• Random Forest  
• Support Vector Machines (SVM)  
• CatBoost  
• LightGBM  
• TabNet

A **stacking ensemble model** combining **CatBoost and LightGBM** was developed to improve prediction performance.

---

# Explainable AI

To improve model transparency and clinical trust, two explainability techniques were applied.

## Grad-CAM++

Used for MRI-based deep learning models.

Grad-CAM++ generates visual heatmaps highlighting the brain regions most responsible for classification decisions.

---

## SHAP (SHapley Additive Explanations)

Applied to clinical data models.

SHAP identifies important features influencing predictions such as:

• Age  
• Cognitive scores  
• Lifestyle factors  
• Genetic risk indicators

---

# Evaluation Metrics

Model performance was evaluated using:

• Accuracy  
• Precision  
• Recall  
• F1 Score  
• ROC-AUC  
• Specificity  
• Balanced Accuracy  
• Log Loss  
• Cohen’s Kappa  
• Matthews Correlation Coefficient

---

# Results

Key findings from experiments include:

• Hybrid CNN–Transformer models achieved **very high classification performance on MRI data**

• Gradient boosting models performed best for **clinical tabular data**

• Multi-modal hybrid approaches outperform single-modality systems

• Explainability methods successfully highlighted important biomarkers and brain regions

---

# Tech Stack

Deep Learning:
PyTorch

Machine Learning:
Scikit-learn  
CatBoost  
LightGBM  
TabNet

Data Processing:
NumPy  
Pandas

Visualization:
Matplotlib  
Seaborn

Computer Vision:
OpenCV

Explainability:
Grad-CAM++  
SHAP
# Hardware

Experiments were conducted using:

NVIDIA Tesla P4 GPUs  
(Kaggle GPU environment)
# Repository Structure

