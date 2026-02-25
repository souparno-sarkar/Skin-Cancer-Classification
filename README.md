# Skin-Cancer-Classification
# Early detection of skin cancer significantly increases survival rates. This project demonstrates how AI can assist dermatologists by providing fast, automated, and reliable preliminary screening.

# FLOWCHART
```mermaid
flowchart TD

A[START] --> B[Data Acquisition]
B --> C[Load HAM10000 Dataset]

C --> D[Data Structuring & Label Engineering]
D --> D1[Merge part_1 + part_2]
D --> D2[Organize Class-wise Folders]
D --> D3[Create Binary Labels]
D --> D4[Maintain 7-Class Labels]

D --> E[Image Preprocessing]
E --> E1[Hair Removal]
E --> E2[Resize 224x224]
E --> E3[Normalization 0-1]
E --> E4[Optional Grayscale]
E --> E5[Data Augmentation]

E --> F[Feature Engineering Strategy]

F --> G1[Deep Learning Pipeline]
G1 --> G11[Raw Images]
G1 --> G12[Automatic Feature Extraction]

F --> G2[Classical ML Pipeline]
G2 --> G21[Flatten Image]
G2 --> G22[Feature Scaling]

G1 --> H[Dataset Splitting]
G2 --> H

H --> H1[Train Set]
H --> H2[Validation Set]
H --> H3[Test Set]

H --> I[Model Development]

I --> I1[Custom CNN]
I --> I2[ResNet50 Transfer Learning]
I --> I3[SVM Linear - Binary]
I --> I4[SVM One-vs-Rest - Multiclass]

I --> J[Model Training]
J --> J1[Forward Propagation]
J --> J2[Loss Computation]
J --> J3[Backpropagation]
J --> J4[SVM Optimization]

J --> K[Hyperparameter Tuning]
K --> K1[Learning Rate]
K --> K2[Batch Size]
K --> K3[Epochs]
K --> K4[Dropout]

K --> L[Performance Evaluation]
L --> L1[Accuracy]
L --> L2[Confusion Matrix]
L --> L3[Precision / Recall / F1]
L --> L4[Overfitting Analysis]

L --> M[Comparative Analysis]
M --> M1[CNN vs ResNet50]
M --> M2[Deep Learning vs SVM]
M --> M3[Binary vs Multiclass]

M --> N[Final Model Selection]
N --> O[Save Best Model]

O --> P[END]
```
