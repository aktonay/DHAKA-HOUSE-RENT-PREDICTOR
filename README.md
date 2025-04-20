
# 🏠 Dhaka House Rent Prediction

In the bustling metropolitan hub of Dhaka, finding the perfect residence that fits one’s needs and budget can be a daunting task. This project introduces a smart solution by predicting house rent prices using advanced machine learning techniques such as **Neural Networks** and **Random Forest**.

---

## 🔍 Introduction

Our goal is to develop an accurate and efficient predictive system that estimates house rent prices based on key attributes such as:

- 📍 Location  
- 📐 Area (sqft)  
- 🛏️ Number of Bedrooms  
- 🛁 Number of Bathrooms  

By combining the predictive strength of **Neural Networks** and **Random Forest**, this project helps users make data-driven rental decisions.

---

## 🧠 Machine Learning Models

### 1. 🔥 Random Forest Regressor
- An ensemble method using multiple decision trees.
- Reduces overfitting by averaging predictions.
- Known for high accuracy and ability to handle mixed datasets.

### 2. 💡 Neural Network (Using Keras)
- Input Layer: 64 Neurons (ReLU)
- Hidden Layer: 32 Neurons (ReLU)
- Output Layer: 1 Neuron (Linear for Regression)
- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)

---

## 📊 Dataset

- **Source**: Kaggle
- **Size**: 28,800 rows × 6 columns
- **Feature Variables**: Location, Area, Beds, Baths  
- **Target Variable**: Rent (in BDT)

---

## ⚙️ Preprocessing Steps

1. **Label Encoding**  
   - Transformed categorical 'Location' into numerical values using `LabelEncoder`.

2. **Area Conversion**  
   - Cleaned and converted 'Area' to float (removed `sqft`, commas).

3. **Price Conversion**  
   - Converted 'Rent' from formats like "45 Thousand", "2.5 Lakh" to numeric using `pd.eval()`.

4. **Feature/Target Split**  
   - Features (X): Location, Area, Beds, Baths  
   - Target (y): Rent

5. **Standardization**  
   - Applied `StandardScaler` on Area, Beds, Baths.

6. **Train-Test Split**  
   - Split: 80% Training / 20% Testing  
   - `random_state=42` for reproducibility

---

## 🏗️ Model Architecture

### ✅ Neural Network (Keras)
- **Input Layer**: 64 neurons, ReLU
- **Hidden Layer**: 32 neurons, ReLU
- **Output Layer**: 1 neuron (Linear)
- **Optimizer**: Adam
- **Loss Function**: Mean Squared Error

### 🌲 Random Forest
- **n_estimators**: 100 Trees
- **random_state**: 42
- Aggregation by **averaging predictions** across trees

---

## 🎛️ Hyperparameter Tuning

| Model            | Tuned Parameters                                           |
|------------------|------------------------------------------------------------|
| Neural Network   | Number of Layers, Neurons, Learning Rate, Batch Size      |
| Random Forest    | n_estimators, max_depth, min_samples_split, random_state  |

---

## 📈 Performance Evaluation

| Metric               | Neural Network | Random Forest |
|----------------------|----------------|----------------|
| Mean Squared Error   | 95,301,841.08  | 43,979,480.01  |
| R-Squared Value      | 0.772          | 0.895          |
| F1-Score             | 0.00034        | 0.0409         |

