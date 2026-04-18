# Image Classification using Random Forest & SVM

## Project Overview
This project focuses on building an image classification system using classical Machine Learning models. The dataset consists of images belonging to five categories as  **dalmatian, dollar_bill, pizza, soccer_ball, sunflower**.

Two models are implemented and compared:
- Random Forest Classifier
- Support Vector Machine (SVM)
- The project evaluates model performance using accuracy, precision, recall, F1-score, confusion matrix and feature importance analysis.

The goal is to classify images based on pixel-level features and analyze model performance.

---

## Dataset Description
- Total samples: **309 images**
- Image size: **64 × 64 pixels**
- Channels: **RGB (3 channels)**
- Flattened feature size: **12288 features per image**
- Classes:
  - dalmatian
  - dollar_bill
  - pizza
  - soccer_ball
  - sunflower

---

## Project Workflow

### 1. Dataset Preprocessing
- Load images from dataset folders
- Resize images to 64×64 pixels
- Normalize pixel values
- Flatten images into 1D feature vectors
- Split dataset into training and testing sets

---

### 2. Model Training

#### Random Forest Classifier
- Hyperparameter tuning using `GridSearchCV`
- Best parameters selected:
  - n_estimators = 100
  - max_depth = 10
  - min_samples_split = 5
  - min_samples_leaf = 2
- Model trained on training dataset

#### SVM Classifier
- Trained using `SVC` from sklearn
- Used as a baseline comparison model

---

### 3. Model Evaluation
- Accuracy score
- Precision, Recall, F1-score
- Confusion Matrix visualization
- Classification Report analysis

---

### 4. Feature Importance
- Extracted using `feature_importances_` from Random Forest
- Visualized important pixel regions contributing to classification

---

### 5. Prediction on New Images
- A function is implemented to:
  - Load new image
  - Apply same preprocessing steps
  - Predict class using trained model

---

## Project Structure
- Images/Images/
  - dalmatian/
  - dollar_bill/
  - pizza/
  - soccer_ball/
  - sunflower/
- Assignment11.ipynb
- README.md
- test_image.jpg

---

## How to Run the Project

### 1. Clone the Repository

git clone https://github.com/parika8ec-hub/AI_Assignment11.git

cd AI_Assignment11

**Install Dependencies**

Make sure you have Python installed (recommended: Python 3.13+).

Install required libraries:

pip install numpy pandas matplotlib scikit-learn opencv-python

**Open and Launch Jupyter Notebook:**

Open Assignment11.ipynb

**Run the Notebook**

Execute all cells step by step:

- Data preprocessing
- Model training
- Evaluation
- Feature importance visualization
- Prediction on new images

**Conclusion**

This project demonstrates how classical machine learning models can be applied to image classification tasks. While both Random Forest and SVM achieve similar accuracy, Random Forest provides better interpretability through feature importance, whereas SVM offers stable classification performance.

**Future Improvements**
- Implement Convolutional Neural Networks (CNNs) for higher accuracy
- Apply data augmentation techniques
- Increase dataset size for better generalization
- Optimize hyperparameters further
