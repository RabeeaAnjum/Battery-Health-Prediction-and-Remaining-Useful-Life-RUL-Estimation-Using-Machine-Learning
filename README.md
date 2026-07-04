# 🔋 Battery Health Prediction and Remaining Useful Life (RUL) Estimation Using Machine Learning

A Machine Learning-based Battery Management System (BMS) that predicts **State of Health (SOH)** and **Remaining Useful Life (RUL)** of Lithium-Ion batteries using operational battery parameters and a **Random Forest Multi-Output Regression** model.

---

## 📌 Project Overview

Lithium-ion batteries degrade over time due to repeated charging and discharging cycles. Accurate prediction of battery degradation is essential for:

- Electric Vehicles (EVs)
- Renewable Energy Storage Systems
- Consumer Electronics
- Industrial Battery Management Systems (BMS)

This project uses Machine Learning to predict:

- **State of Health (SOH)**
- **Remaining Useful Life (RUL)**

using real battery operational data from the **NASA Ames Prognostics Data Repository**.

---

## 🎯 Objectives

- Predict battery State of Health (SOH)
- Estimate Remaining Useful Life (RUL)
- Analyze battery degradation patterns
- Perform feature engineering for improved prediction
- Develop an AI-based Battery Management System

---

## 📂 Dataset

**Source:** NASA Ames Prognostics Center of Excellence (PCoE)

Battery Cells Used:

- B5
- B6
- B7

The dataset contains charge-discharge cycle information including electrical and thermal parameters.

### Input Features

| Feature | Description |
|----------|-------------|
| battery_id | Battery Identifier |
| cycle | Charge-Discharge Cycle |
| chI | Charging Current |
| chV | Charging Voltage |
| chT | Charging Temperature |
| disI | Discharging Current |
| disV | Discharging Voltage |
| disT | Discharging Temperature |

### Target Variables

| Target | Description |
|----------|-------------|
| SOH | State of Health |
| RUL | Remaining Useful Life |
| BCt | Battery Charging Time |

---

# 🧠 Machine Learning Pipeline

```
Load Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Label Encoding
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
Outlier Detection (IQR)
      │
      ▼
Feature Engineering
      │
      ▼
Feature Scaling
      │
      ▼
Train-Test Split
      │
      ▼
Random Forest Regression
      │
      ▼
Prediction
      │
      ▼
Model Evaluation
      │
      ▼
Feature Importance Analysis
```

---

# 📊 Exploratory Data Analysis (EDA)

The project includes:

- Correlation Heatmap
- Cycle vs SOH
- Cycle vs RUL
- Charging Temperature vs SOH
- Battery-wise SOH Comparison
- Boxplots for Outlier Analysis

---

# ⚙️ Feature Engineering

Three new features were created:

| Feature | Formula |
|----------|----------|
| Voltage_Diff | chV − disV |
| Temp_Diff | chT − disT |
| Current_Diff | chI − disI |

These engineered features help the model better understand battery degradation behavior.

---

# 🤖 Machine Learning Model

Model Used:

- **Random Forest Regressor**
- Multi-Output Regression

### Why Random Forest?

- Handles non-linear relationships
- Robust to noisy data
- Supports multiple outputs
- Provides feature importance
- High prediction accuracy

---

# 📈 Model Evaluation

The model is evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

Additionally, the project visualizes:

- Actual vs Predicted SOH
- Actual vs Predicted RUL

---

# 📌 Feature Importance

One of the most significant findings:

| Feature | Importance |
|----------|-------------|
| Cycle | **≈95.19%** |
| Battery ID | ≈4.60% |
| Other Features | <0.21% |

The analysis shows that battery degradation is highly dependent on the charge-discharge cycle count.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab

---

# 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Battery-Health-Prediction.git
```

Move into the project directory:

```bash
cd Battery-Health-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Project

Open the Jupyter Notebook or Google Colab notebook and execute all cells sequentially.

Or run:

```bash
python battery_health_prediction.py
```

---

# 📁 Project Structure

```
Battery-Health-Prediction/
│
├── Dataset/
│   └── Battery_dataset.csv
│
├── Notebook/
│   └── Battery_Health_Prediction.ipynb
│
├── Images/
│   ├── CorrelationHeatmap.png
│   ├── SOH_vs_Cycle.png
│   ├── RUL_vs_Cycle.png
│   ├── FeatureImportance.png
│   └── Predictions.png
│
├── Model/
│   └── random_forest_model.pkl
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

# 📊 Results

✔ Accurate prediction of Battery SOH

✔ Reliable estimation of Remaining Useful Life

✔ Effective feature engineering

✔ Professional Machine Learning pipeline

✔ Suitable for Intelligent Battery Management Systems

---

# 🚀 Future Improvements

- Deep Learning (LSTM & GRU)
- Real-Time IoT Battery Monitoring
- Edge AI Deployment
- Mobile/Web Dashboard
- Cloud-based Battery Analytics
- Larger Battery Datasets
- Real-Time Prediction API

---

# 📚 References

- NASA Ames Prognostics Data Repository
- Scikit-Learn Documentation
- Random Forest (Breiman, 2001)
- Nature Energy – Battery Cycle Life Prediction
- Journal of Power Sources

---

# 👩‍💻 Author

**Rabeea Anjum**

BS Computer Systems Engineering

Department of Computer Systems Engineering

Faculty of Engineering & Technology

The Islamia University of Bahawalpur

---

# ⭐ If you found this project useful

Please consider giving this repository a **Star ⭐** on GitHub.

It helps support the project and encourages further development.
