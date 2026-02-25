# Skin-Cancer-Classification
# Early detection of skin cancer significantly increases survival rates. This project demonstrates how AI can assist dermatologists by providing fast, automated, and reliable preliminary screening.

# FLOWCHART
```mermaid
flowchart TD

A[START] --> B[Load HAM10000 Dataset]

B --> C[Data Structuring]
C --> C1[Merge part_1 + part_2]
C --> C2[Create Binary & Multiclass Labels]

C2 --> D[Image Preprocessing]
D --> D1[Hair Removal]
D --> D2[Resize 224x224]
D --> D3[Normalization]
D --> D4[Data Augmentation]

D4 --> E[Feature Preparation]
E --> E1[Deep Learning: Raw Images]
E --> E2[Classical ML: Flatten Images]

E2 --> F[Train / Validation / Test Split]

F --> G[Model Development]
G --> G1[Custom CNN]
G --> G2[ResNet50]
G --> G3[SVM Linear]
G --> G4[SVM Multiclass]

G4 --> H[Model Training & Tuning]

H --> I[Performance Evaluation]
I --> I1[Accuracy]
I --> I2[Confusion Matrix]
I --> I3[Precision / Recall / F1]

I3 --> J[Model Comparison]

J --> K[Select Best Model]

K --> L[END]
```
