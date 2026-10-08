# Skin Cancer Detection from Images

## Overview
This project focuses on building a machine learning model to detect skin cancer from images. It classifies skin lesion images into two categories: **Benign** (non-cancerous) and **Malignant** (cancerous). The classification is performed using a Support Vector Machine (SVM) algorithm.

## Dataset
The code expects the dataset to be structured into training and testing directories, typically provided in a Kaggle environment:
- `../input/data/train/benign`
- `../input/data/train/malignant`
- `../input/data/test/benign`
- `../input/data/test/malignant`

Each directory contains image files of skin lesions corresponding to their respective class.

## Technologies and Libraries Used
The project is implemented in Python and relies on the following libraries:
- **NumPy** & **Pandas**: Data manipulation and array operations.
- **Pillow (PIL)**: Image loading and basic processing.
- **Matplotlib** & **Seaborn**: Data visualization (displaying sample images and plotting class distributions).
- **Scikit-learn (sklearn)**: Machine learning model building and evaluation.

## Methodology
1. **Data Loading**: Images are loaded using Pillow, converted to RGB, and stored as NumPy arrays. Labels are assigned (`0` for benign, `1` for malignant).
2. **Data Exploration**: 
   - A subset of training images is displayed to visualize the data.
   - Bar charts are generated to show the class distribution (benign vs. malignant) in both the training and testing sets.
3. **Model Training**: The images are flattened into 1D arrays to be used as features. A Support Vector Classifier (`SVC` from `sklearn`) is then trained on this data.
4. **Evaluation**: The trained model predicts the classes for the testing set. The performance is evaluated using the `accuracy_score` metric.

## How to Run
1. Ensure you have the required dataset structure in place as mentioned above.
2. Install the necessary dependencies (if not already installed):
   ```bash
   pip install numpy pandas matplotlib seaborn Pillow scikit-learn
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook detect-skin-cancer-from-images.ipynb
   ```
4. Run all the cells in the notebook to load the data, visualize it, train the model, and view the final accuracy score.