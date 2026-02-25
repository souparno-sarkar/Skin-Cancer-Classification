# Skin-Cancer-Classification
# Early detection of skin cancer significantly increases survival rates. This project demonstrates how AI can assist dermatologists by providing fast, automated, and reliable preliminary screening.

# FLOWCHART

   START
     ↓
1️.  Data Acquisition
        ↓
    Load HAM10000 Dataset
        ↓
2️. Data Structuring & Label Engineering
   ├── Merge image directories (part_1 + part_2)
   ├── Organize into class-wise folders
   ├── Create Binary Labels (Benign vs Malignant)
   └── Verify class distribution (handle imbalance if needed)
   ↓
3️. Image Preprocessing Pipeline
   ├── Hair Removal (Morphological operations + Inpainting)
   ├── Image Resizing (224 × 224)
   ├── Pixel Normalization (0–1 scaling)
   ├── Optional Grayscale Conversion (Experimental Study)
   └── Data Augmentation (Flip, Rotation, etc.)
   ↓
4️. Feature Engineering Strategy
   ├── Deep Learning Pipeline
   │      → Raw preprocessed images
   │      → Automatic feature extraction via CNN filters
   │
   └── Classical ML Pipeline
          → Image Flattening (1D feature vector)
          → Feature Scaling (if applied)
   ↓
5️. Dataset Splitting
   ├── Train Set
   ├── Validation Set
   └── Test Set
        (Applied for both Binary & Multiclass tasks)
   ↓
6️. Model Development
   ├── A. Custom Convolutional Neural Network (CNN)
   ├── B. ResNet50 (Transfer Learning – ImageNet pretrained)
   ├── C. SVM (Linear Kernel – Binary Classification)
   └── D. SVM (One-vs-Rest – Multiclass Classification)
   ↓
7️. Model Training
   ├── Forward Propagation
   ├── Loss Computation
   ├── Backpropagation (for CNN/ResNet)
   └── Decision Boundary Optimization (for SVM)
   ↓
8️. Model Validation & Hyperparameter Tuning
   ├── Learning Rate tuning
   ├── Batch Size adjustment
   ├── Dropout Regularization
   └── Epoch optimization
   ↓
9️. Performance Evaluation
   ├── Accuracy
   ├── Confusion Matrix
   ├── Precision
   ├── Recall
   ├── F1-Score
   └── Overfitting / Underfitting Analysis
   ↓
10. Comparative Analysis
   ├── CNN vs ResNet50
   ├── Deep Learning vs SVM
   └── Binary vs Multiclass Performance
   ↓
11. Final Model Selection
   ├── Select best-performing architecture
   └── Save trained model
   ↓
  END



