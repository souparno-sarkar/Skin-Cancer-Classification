# Skin-Cancer-Classification
# Early detection of skin cancer significantly increases survival rates. This project demonstrates how AI can assist dermatologists by providing fast, automated, and reliable preliminary screening.

# FLOWCHART

START
  ↓
1️⃣ Data Acquisition
  ↓
Load HAM10000 Dataset (Images + Metadata CSV)
  ↓
2️⃣ Data Structuring & Label Engineering
  ├── Merge image directories (part_1 + part_2)
  ├── Organize images into class-wise folders
  ├── Create Binary Labels (Benign vs Malignant)
  └── Maintain Multiclass Labels (7 Classes)
  ↓
3️⃣ Image Preprocessing Pipeline
  ├── Hair Removal (Morphological Closing + Inpainting)
  ├── Resize Images to 224 × 224
  ├── Pixel Normalization (0–1 Scaling)
  ├── Optional Grayscale Conversion (Experimental)
  └── Data Augmentation (Flip, Rotation, etc.)
  ↓
4️⃣ Feature Engineering Strategy
  ├── 🔵 Deep Learning Pipeline
  │       → Use Raw Preprocessed Images
  │       → Automatic Feature Extraction via CNN Filters
  │
  └── 🟢 Classical ML Pipeline
          → Flatten Image into 1D Feature Vector
          → Apply Feature Scaling (if required)
  ↓
5️⃣ Dataset Splitting
  ├── Train Set
  ├── Validation Set
  └── Test Set
       (Applied for both Binary & Multiclass Tasks)
  ↓
6️⃣ Model Development
  ├── A. Custom CNN
  ├── B. ResNet50 (Transfer Learning – ImageNet Pretrained)
  ├── C. SVM (Linear Kernel – Binary Classification)
  └── D. SVM (One-vs-Rest – Multiclass Classification)
  ↓
7️⃣ Model Training
  ├── Forward Propagation
  ├── Loss Computation
  ├── Backpropagation (CNN / ResNet50)
  └── Decision Boundary Optimization (SVM)
  ↓
8️⃣ Hyperparameter Tuning
  ├── Learning Rate Adjustment
  ├── Batch Size Tuning
  ├── Epoch Optimization
  └── Dropout Regularization
  ↓
9️⃣ Performance Evaluation
  ├── Accuracy
  ├── Confusion Matrix
  ├── Precision
  ├── Recall
  ├── F1-Score
  └── Overfitting / Underfitting Analysis
  ↓
🔟 Comparative Analysis
  ├── CNN vs ResNet50
  ├── Deep Learning vs SVM
  └── Binary vs Multiclass Performance
  ↓
1️⃣1️⃣ Final Model Selection
  ├── Select Best Performing Model
  └── Save Trained Model (.h5 / .pt / .pkl)
  ↓
END
