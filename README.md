# 🩻 RadAlert: EHR + MRI Fusion for Context-Aware Breast Cancer Detection

**RadAlert** is a **multimodal deep learning system** that uniquely fuses ** MRI imaging** and **EHR data** for **Breast Cancer** detection 
through a dual-branch late-fusion model, enabling context-aware reasoning between patient history and tumor morphology.
It outputs the **probability of malignancy**, where values **above 0.5 indicate a high likelihood of breast cancer**, providing interpretable, data-driven clinical insight.

RadAlert is intended for medical AI researchers, data scientists, and clinicians interested in exploring or developing multimodal breast cancer detection models that integrate MRI imaging and EHR data for interpretable, probability-based predictions.

The EHR data gives RadAlert extra “context” about the person — things like age, tumor size, and prior history — while the MRI images show what the tumor physically looks like. When RadAlert fuses them, it doesn’t just look at pictures; it learns to connect what it sees in the MRI with what it knows from the patient’s record — for example, if a certain tumor pattern plus certain clinical traits usually mean cancer, it becomes more confident (the output probability > 0.5). So, the EHR branch teaches the model why something might be cancer, and the MRI branch shows where and how it appears — together they make the prediction smarter and more accurate.

---

##  Features
- **Dual-Branch Fusion:** Independent EHR and MRI encoders fused through a learnable layer.  
- **Context-Aware Predictions:** Integrates patient-level context with tumor visual cues.  
- **Automatic Model Loading:** Detects and loads full model or state_dict automatically.  
- **Lightweight Fallback:** Uses `SimpleCNN` when full model unavailable.  
- **Explainable Output:** Displays malignancy probability, label, and textual interpretation.

---

##  Model Overview
| Branch | Input | Focus | Output |
|--------|--------|--------|--------|
|  **EHR Branch** | Clinical metadata (e.g., tumor size, demographics) | Health patterns | Clinical embedding |
|  **MRI Branch** | DICOM MRI scans | Spatial and morphological cues | Visual embedding |
|  **Fusion Layer** | Concatenated embeddings | Cross-modality reasoning | Malignancy probability |





## 🧬 Dataset Source

The datasets used in this project are derived from the  
**[Duke-Breast-Cancer-MRI Collection (The Cancer Imaging Archive - TCIA)](https://www.cancerimagingarchive.net/collection/duke-breast-cancer-mri/)**.  

This dataset includes:
- Dynamic-contrast-enhanced breast MRI scans (DICOM format)  
- Clinical metadata containing lesion characteristics and diagnostic labels  

EHR-like features (e.g., tumor size, recurrence history, and demographics) were extracted from the accompanying metadata and merged with MRI image-derived features by **Patient ID** to enable cross-modal learning.





---

##  Files
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
