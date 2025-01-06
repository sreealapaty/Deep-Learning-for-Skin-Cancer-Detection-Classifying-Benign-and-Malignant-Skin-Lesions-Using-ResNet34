# Deep Learning for Skin Cancer Detection  
> **Classifying Benign and Malignant Skin Lesions Using ResNet-34**

---

## 📄 Project Overview  
Skin cancer is one of the most prevalent cancers worldwide, and early detection plays a critical role in effective treatment. This project leverages **deep learning** to classify dermatoscopic skin lesions as **benign** or **malignant** using the **ResNet-34 architecture**. By assisting dermatologists with precise and timely predictions, this project contributes to improving patient outcomes.

---

## 🌟 Key Highlights  

### Dataset  
- **[HAM10000](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)**: A dataset of **10,015 dermatoscopic images**, including metadata and diagnostic labels.  
- Data preprocessing involved parsing metadata, converting diagnostic labels to binary, and applying an **80/20 train-validation split** with stratified sampling.

### Binary Classification  
- **Malignant Classes:** Melanoma, Basal Cell Carcinoma (BCC), and Actinic Keratosis (AKIEC).  
- **Benign Classes:** All other lesion types.

### Deep Learning Model  
- **Architecture:** Pretrained ResNet-34 tailored for binary classification.  
- **Enhancements:**  
  - Data augmentation techniques (rotation, flipping, and color jitter).  
  - Class weighting to address dataset imbalance.  
  - Regularization for improved generalization.  

### Performance Metrics  
- **Validation Accuracy:** 74%  
- **Test Accuracy:** 72%  
- **ROC-AUC Scores:**  
  - Validation: 0.8311  
  - Test: 0.8347  

---

## 🎯 Project Objective  
To develop a reliable deep learning model for distinguishing **benign** from **malignant** skin lesions, enabling early detection of skin cancer and supporting dermatologists in clinical decision-making.

---

## 🛠 Implementation Steps  

### Data Preprocessing  
1. Extracted metadata and images from the **HAM10000 dataset**.  
2. Assigned binary labels:  
   - `1` for malignant (melanoma, BCC, AKIEC).  
   - `0` for benign.  
3. Addressed class imbalance with weighted loss functions.  

### Model Training  
- Modified **ResNet-34** for binary classification by replacing the fully connected layer.  
- Applied augmentations: resizing, random rotation, horizontal flips, and color jitter.  
- Optimized using **Adam optimizer** and **ReduceLROnPlateau scheduler**.  

### Performance Evaluation  
- Metrics:
  - Confusion Matrix  
  - Precision, Recall, and F1-Score  
  - ROC-AUC  
- Visualized training and validation accuracy/loss across epochs.

### Visualization  
- Sample predictions with **actual and predicted labels** were displayed for interpretability.  
- Misclassified cases were analyzed to identify areas for improvement.

---

## 📊 Results  

### Validation Set  
- **Confusion Matrix:**  
  - Benign: Precision - 93%, Recall - 73%  
  - Malignant: Precision - 42%, Recall - 78%  
- **ROC-AUC:** 0.8311  

### Test Set  
- **Confusion Matrix:**  
  - Benign: Precision - 95%, Recall - 69%  
  - Malignant: Precision - 41%, Recall - 86%  
- **ROC-AUC:** 0.8347  

---

## 🚀 Future Enhancements  
1. **Address Class Imbalance:**  
   - Explore advanced techniques like oversampling, undersampling, or **Synthetic Minority Oversampling (SMOTE)**.  
2. **Experiment with Architectures:**  
   - Test deeper models like ResNet-50 or EfficientNet.  
3. **Hyperparameter Optimization:**  
   - Fine-tune learning rates, batch sizes, and number of epochs.  
4. **Augment Data:**  
   - Implement advanced augmentation strategies for increased variability.

---

## 🛠 Tools and Technologies  
- **Programming Language:** Python  
- **Frameworks:** PyTorch, Scikit-learn  
- **Libraries:** Pandas, NumPy, Matplotlib, Torchvision  
- **Dataset:** [HAM10000](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)

## 📚 References
- **HAM10000 Dataset**
- **PyTorch Documentation**
- **ISIC Archive**
- **Classification Metrics in Python**
