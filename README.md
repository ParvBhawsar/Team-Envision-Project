# Team-Envision-Project
# 🩺 Chest X-Ray Classification (Normal | Pneumonia | Tuberculosis)

## 📌 Project Overview  
This project builds a **deep learning model** that classifies chest X-ray images into three categories:  
- **Normal**  
- **Pneumonia**  
- **Tuberculosis**  

The aim is to support doctors with **faster and more accurate diagnoses** using AI.  

Dataset is taken from **Kaggle/GitHub open-source chest X-ray datasets**.  

---

## ⚙️ Workflow  
1. **Data Preprocessing**  
   - Images resized to 224×224  
   - Normalization applied (pixel values scaled to [0,1])  
   - Data Augmentation (rotation, flip, zoom) for better generalization  
   - Data split into **Train (70%) | Validation (15%) | Test (15%)**

2. **Model Architecture**  
   - Base: **ResNet18** pretrained on ImageNet  
   - Modified final layer for **3-class classification**  
   - Used **Dropout, Batch Normalization, Weight Decay** to avoid overfitting  

3. **Evaluation Metrics**  
   - Accuracy  
   - Precision, Recall, F1-score  
   - Confusion Matrix  
   - ROC-AUC Curve  

4. **Ethical Considerations**  
   - Model performance depends on dataset quality (possible bias).  
   - AI should support doctors, **not replace them**.  
   - Fairness, transparency, and explainability are critical.  

---

## 📊 Results (Sample)  
- Accuracy: ~85% (depends on training time/dataset split)  
- Balanced performance across 3 classes  
- Visualized training curves + confusion matrix  

---

## 🚀 How to Run  

### 1. Clone Repository  
```bash
git clone https://github.com/yourusername/envision_cxr.git
cd envision_cxr
```

### 2. Install Requirements  
```bash
pip install -r requirements.txt
```

### 3. Open Jupyter Notebook  
```bash
jupyter notebook baseline_envision_cxr.ipynb
```

### 4. Train the Model  
- Run all cells step by step (`Shift+Enter`)  
- The notebook will:  
  - Load and preprocess dataset  
  - Train ResNet18 model  
  - Show accuracy/precision/recall/F1  
  - Plot confusion matrix  

---

## 📂 Repository Structure  
```
envision_cxr/
│── baseline_envision_cxr.ipynb   # Main code (Jupyter Notebook)
│── requirements.txt              # Python dependencies
│── README.md                     # Project documentation
```

---

## 📌 Future Improvements  
- Try EfficientNet for better accuracy  
- Add Grad-CAM for explainability  
- Deploy model as a web app  

---

## 🧑‍⚕️ Disclaimer  
This project is for **educational purposes** only.  
It is **not a certified medical tool**.  
Final diagnosis should always be confirmed by medical professionals.  
