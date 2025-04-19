# CNN for Breast Density Classification from Mammograms

---

## Dataset

- **Dataset:** MIAS Mammographic Dataset  
- **Format:** Converted from `.pgm` to `.jpg` RGB images  
- **Image Size:** 224x224 pixels  
- **Train/Validation Split:** 80% training, 20% validation  
- **Batch Size:** 8  

---

## Model Architecture

The CNN model contains four convolutional layers with increasing filter sizes to extract progressively complex image features.

| Layer       | Filters | Activation | Purpose                       |
|-------------|---------|------------|-------------------------------|
| Conv2D #1   | 32      | ReLU       | Basic edge detection          |
| Conv2D #2   | 64      | ReLU       | Mid-level feature extraction  |
| Conv2D #3   | 128     | ReLU       | High-level pattern learning   |
| Conv2D #4   | 128     | ReLU       | Enhanced feature extraction   |

- **Flattening Layer** to prepare data for Dense layers  
- **Optimizer:** Adadelta (initial learning rate = 1.0)  
- **Loss Function:** Categorical Crossentropy  
- **Activation Function:** ReLU for convolutional layers  

---

## Training Metrics

| Metric   | Training       | Validation     |
|----------|----------------|----------------|
| Accuracy | 0.233          | 0.262          |
| Loss     | 1.390          | 1.388          |

---

## Evaluation on Test Set

| Metric   | Value           |
|----------|-----------------|
| Accuracy | 0.262           |
| Loss     | 1.388           |
