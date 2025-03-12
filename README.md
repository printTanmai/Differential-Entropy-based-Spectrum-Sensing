# Differential-Entropy-based-Spectrum-Sensing using Machine Learning
## Overview
This repository contains a machine learning-based spectrum sensing model for cognitive radios. The project preprocesses spectrum data, extracts relevant features, and applies classification algorithms to detect signal presence. It follows a **supervised learning approach** using **differential entropy features**, inspired by recent research in cognitive radio networks. The model determines whether a channel is occupied by analyzing the **differential entropy of the channel**.

## Features
- Loads and processes spectrum sensing data from MATLAB `.mat` files.
- Extracts and normalizes the dataset for feature engineering.
- Implements **K-Nearest Neighbors (KNN), Logistic Regression, and Random Forest** classifiers.
- Compares model performance in different **Signal-to-Noise Ratio (SNR)** conditions.
- Utilizes **differential entropy of the channel** to classify whether a channel is occupied.

## Installation
Ensure you have Python and the required dependencies installed:
```bash
pip install numpy pandas scipy scikit-learn matplotlib
```

## Dataset
The model uses spectrum sensing data stored in `.mat` format. The primary dataset consists of signal observations under different noise conditions. The preprocessing steps include:
1. Extracting the first column from the `.mat` dataset.
2. Normalizing the signal data.
3. Reshaping and saving it as `output.csv` for further analysis.

## Usage
### Running the Model
Clone the repository and navigate to the project directory:
```bash
git clone https://github.com/printTanmai/Differential-Entropy-based-Spectrum-Sensing.git
cd Differential-Entropy-based-Spectrum-Sensing
```

Run the Jupyter Notebook:
```bash
jupyter notebook "Machine Learning.ipynb"
```

### Steps in the Notebook
1. **Load Data**: Reads `.mat` files and extracts signal data.
2. **Preprocessing**: Normalizes the data and reshapes it for ML models.
3. **Feature Extraction**: Uses **differential entropy** as a key metric for classification.
4. **Model Training**: Applies **KNN, Logistic Regression, and Random Forest** classifiers.
5. **Evaluation**: Compares model performance using detection probability vs. SNR graphs.

## Results
- **KNN and Logistic Regression achieved higher accuracy even at lower SNR levels** compared to Random Forest.
- The **differential entropy feature** improves detection performance over traditional energy-based methods.
- The model effectively detects primary user activity under **generalized Gaussian noise conditions**.

### Detection Probability vs SNR

![Detection Probability vs SNR](https://github.com/user-attachments/assets/59ba9f4a-b4f9-4489-b22d-ce90a20e1f58)

## Contributing
Feel free to fork this repository and improve the model.
