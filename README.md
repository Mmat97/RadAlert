# 🩻 RadAlert: EHR + MRI Fusion for Context-Aware Breast Cancer Detection

**RadAlert** is a **unique multimodal deep learning system** that predicts breast MRI malignancy by combining **radiological imaging data** with **electronic health record (EHR)** features.  
Unlike standard multimodal models, RadAlert uses a **dual-branch late-fusion design**—one branch for structured EHR data and another for imaging features—allowing each to learn independently before merging.  
This enables **deeper, context-aware reasoning** between patient history and tumor morphology for more interpretable cancer detection and recurrence prediction.

---

## 🚀 Features
- **Dual-Branch Fusion:** Independent EHR and MRI encoders fused through a learnable layer.  
- **Context-Aware Predictions:** Integrates patient-level context with tumor visual cues.  
- **Automatic Model Loading:** Detects and loads full model or state_dict automatically.  
- **Lightweight Fallback:** Uses `SimpleCNN` when full model unavailable.  
- **Explainable Output:** Displays malignancy probability, label, and textual interpretation.

---

## 🧠 Model Overview
| Branch | Input | Focus | Output |
|--------|--------|--------|--------|
| 🧬 **EHR Branch** | Clinical metadata (e.g., tumor size, demographics) | Health patterns | Clinical embedding |
| 🩻 **MRI Branch** | DICOM MRI scans | Spatial and morphological cues | Visual embedding |
| 🔗 **Fusion Layer** | Concatenated embeddings | Cross-modality reasoning | Malignancy probability |





## 🧬 Dataset Source

The datasets used in this project are derived from the  
**[Duke-Breast-Cancer-MRI Collection (The Cancer Imaging Archive - TCIA)](https://www.cancerimagingarchive.net/collection/duke-breast-cancer-mri/)**.  

This dataset includes:
- Dynamic-contrast-enhanced breast MRI scans (DICOM format)  
- Clinical metadata containing lesion characteristics and diagnostic labels  

EHR-like features (e.g., tumor size, recurrence history, and demographics) were extracted from the accompanying metadata and merged with MRI image-derived features by **Patient ID** to enable cross-modal learning.





---

## 📂 Files
RadAlert_Main3.ipynb → Main notebook (training + inference)
radalert_mri_fusion.pth → Saved model weights (full model or state_dict)
fastMRI_breast_IDS_001_150_DCM.tar → MRI dataset (DICOM)
fastMRI_breast_labels.xlsx → EHR + ground truth labels
Sample_SCREENSHOT.png → Example output visualization


<img width="403" height="213" alt="Sample_SCREENSHOT" src="https://github.com/user-attachments/assets/2a898708-f2a5-48ba-960b-b873d72b1afa" />







🧾 Example Output
🤖 Model Probability (malignancy): 0.5135
🩺 Predicted Label: ⚠️ ALERT
📊 Actual Label: 2 → Benign (Non-cancerous abnormality)
⚠️ The model predicts this MRI has a high likelihood of MALIGNANCY (cancerous lesion).
