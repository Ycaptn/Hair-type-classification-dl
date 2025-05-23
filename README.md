
## Model
- **Architecture**: `EfficientNetB7`, fine-tuned on the hairstyle dataset.
- **Framework**: TensorFlow 2.x.
- **Training Details**:
- Used data augmentation (`RandomFlip`, `RandomRotation`, `RandomHeight`, `RandomWidth`, `RandomZoom`) to mitigate overfitting.
- Trained for 5 epochs (baseline model) and 20 epochs (augmented model) with a batch size of 32.
- Optimizer: Adam with default learning rate.
- Callbacks: `ModelCheckpoint`.

- **Performance**:
- Training Accuracy: 90%.
- Test Accuracy: 23% (195 samples; results may be skewed due to prior train/test overlap).
- F1-Scores: Range from 0.15 to 0.36 across classes, with Class 3 performing best (F1: 0.36).
- **Challenges**: Severe overfitting due to limited dataset size and class imbalance.
- **Ongoing Improvements**: Hyperparameter tuning (learning rate, dropout rate), applying class weights to handle imbalance, and exploring additional augmentation (e.g., color jittering).

## Setup Instructions
1. **Clone the Repository**:
 ```bash
 git clone https://github.com/Ycaptn/Hair-type-classification-dl.git
 cd Hair-type-classification-dl
