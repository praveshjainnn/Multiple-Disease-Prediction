# 🧑‍⚕️ Multiple Disease Prediction System

A machine learning web application that predicts the likelihood of **Diabetes**, **Heart Disease**, and **Parkinson's Disease** based on patient health data — built with Python and Streamlit.

---

## 🔍 Overview

This app takes medical inputs from the user and uses pre-trained ML models to instantly predict whether a person is likely to have one of three diseases. It is designed to be simple, fast, and accessible — no medical expertise needed to run it.

| Disease | Algorithm | Dataset Size |
|---------|-----------|-------------|
| Diabetes | Support Vector Machine (SVM) | 768 records |
| Heart Disease | Logistic Regression | 303 records |
| Parkinson's Disease | Support Vector Machine (SVM) | 195 voice recordings |

---

## 📁 Project Structure

```
multiple-disease-prediction-streamlit-app/
│
├── app.py                          # Main Streamlit web application
├── requirements.txt                # Python dependencies
│
├── dataset/
│   ├── diabetes.csv                # Pima Indians Diabetes Dataset
│   ├── heart.csv                   # Cleveland Heart Disease Dataset
│   └── parkinsons.csv              # UCI Parkinson's Voice Dataset
│
├── saved_models/
│   ├── diabetes_model.sav          # Trained SVM model for diabetes
│   ├── heart_disease_model.sav     # Trained model for heart disease
│   └── parkinsons_model.sav        # Trained SVM model for Parkinson's
│
└── colab_files_to_train_models/
    ├── Multiple disease prediction system - diabetes.ipynb
    ├── Multiple disease prediction system - heart.ipynb
    └── Multiple disease prediction system - Parkinsons.ipynb
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/praveshjainnn/Multiple-Disease-Prediction.git
cd Multiple-Disease-Prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app

```bash
streamlit run app.py
```

The app will open in your browser at **http://localhost:8501**

---

## 🖥️ How to Use

1. Open the app in your browser
2. Select a disease from the **left sidebar**
3. Enter the patient's medical values in the input fields
4. Click the **Test Result** button
5. The prediction appears instantly in a green result box

---

## 🩺 Disease Modules

### 💉 Diabetes Prediction
Uses 8 health features to predict diabetes:
- Pregnancies, Glucose, Blood Pressure, Skin Thickness
- Insulin, BMI, Diabetes Pedigree Function, Age

### ❤️ Heart Disease Prediction
Uses 13 clinical features including:
- Age, Sex, Chest Pain Type, Resting Blood Pressure
- Cholesterol, Fasting Blood Sugar, ECG Results
- Max Heart Rate, Exercise Angina, ST Depression, and more

### 🧠 Parkinson's Disease Prediction
Uses 22 voice signal measurements including:
- Fundamental frequency (Fo, Fhi, Flo)
- Jitter & Shimmer (voice trembling indicators)
- Noise-to-Harmonic Ratio (NHR / HNR)
- Nonlinear features: RPDE, DFA, spread1, spread2, D2, PPE

---

## 📦 Dependencies

```
numpy==1.26.3
scikit-learn==1.3.2
streamlit==1.29.0
streamlit-option-menu==0.3.6
```

---

## 🧪 Training the Models

The models were trained in Google Colab. To retrain:

1. Open the notebooks in the `colab_files_to_train_models/` folder
2. Run all cells in Google Colab
3. Download the generated `.sav` files
4. Replace the files in the `saved_models/` folder

---

## 📊 Datasets

| Dataset | Source | Records | Target |
|---------|--------|---------|--------|
| Diabetes | [Pima Indians — UCI ML Repo](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) | 768 | 1 = Diabetic, 0 = Not |
| Heart Disease | [Cleveland — UCI ML Repo](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset) | 303 | 1 = Disease, 0 = Healthy |
| Parkinson's | [UCI ML Repo (Max Little)](https://www.kaggle.com/datasets/vikasukani/parkinsons-disease-data-set) | 195 | 1 = Parkinson's, 0 = Healthy |

---

## 📌 Notes

- All models are pre-trained and ready to use — no retraining needed to run the app
- The Parkinson's model uses feature normalization (MinMaxScaler) during training
- Input values of `0` in the diabetes dataset may indicate missing data in the original source

---

## 🙌 Acknowledgements

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php) for the datasets
- [Streamlit](https://streamlit.io/) for the web framework
- [scikit-learn](https://scikit-learn.org/) for the ML algorithms
