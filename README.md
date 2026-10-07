# Household Electric Power Consumption Prediction

## 📌 Project Overview

This project uses historical household electricity consumption data to build a **Machine Learning model** that predicts **Global Active Power**, which represents the household's total electricity consumption.

The project focuses on understanding the relationship between electricity measurements, time-based features, and household power consumption.

The final model uses **Linear Regression** for prediction.

---

## 🎯 Objective

The main objective of this project is to:

* Analyze household electricity consumption data.
* Clean and preprocess the dataset.
* Perform Exploratory Data Analysis (EDA).
* Extract useful time-based features such as **hour** and **day**.
* Analyze relationships between electrical measurements.
* Train a Machine Learning model.
* Predict **Global Active Power** from the available features.
* Evaluate the model using **Mean Squared Error (MSE)** and **R² Score**.

---

## 📊 Dataset

The project uses the **Household Electric Power Consumption** dataset.

The dataset contains electrical measurements collected from a household over time.

### Important Features

| Feature               | Description                                 |
| --------------------- | ------------------------------------------- |
| `Date`                | Date of the measurement                     |
| `Time`                | Time of the measurement                     |
| `Global_active_power` | Total household electricity consumption     |
| `Voltage`             | Voltage measurement                         |
| `Sub_metering_1`      | Electricity consumption from sub-metering 1 |
| `Sub_metering_2`      | Electricity consumption from sub-metering 2 |
| `Sub_metering_3`      | Electricity consumption from sub-metering 3 |
| `DateTime`            | Combined date and time                      |
| `hour`                | Hour extracted from `DateTime`              |
| `day`                 | Day of the week extracted from `DateTime`   |

---

## 🔧 Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 🛠️ Project Workflow

The project follows these main steps:

### 1. Import Libraries

The required Python libraries are imported for:

* Data processing
* Visualization
* Statistical analysis
* Machine Learning

### 2. Load Dataset

The household power consumption dataset is loaded from a `.txt` file using Pandas.

The dataset uses `;` as the separator and `?` values are treated as missing values.

### 3. Data Exploration

Initial exploration is performed using:

* `head()`
* `shape`
* `info()`
* `describe()`
* Missing-value analysis

### 4. Exploratory Data Analysis

Different visualizations are used to understand the data, including:

* Distribution of Global Active Power
* Missing-value heatmap
* Power consumption over time
* Hour vs. power consumption
* Day vs. power consumption
* Correlation heatmap

### 5. Data Preprocessing

The following preprocessing steps are performed:

* Combine `Date` and `Time` into a new `DateTime` feature.
* Remove rows with invalid `DateTime`.
* Extract `hour` from `DateTime`.
* Extract `day` from `DateTime`.
* Remove missing values from the target and selected input features.

### 6. Feature Selection

The following features are used as input variables:

```text
hour
day
Voltage
Sub_metering_1
Sub_metering_2
Sub_metering_3
```

### 7. Target Variable

The target variable is:

```text
Global_active_power
```

### 8. Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

A `random_state` of 42 is used for reproducibility.

### 9. Feature Scaling

`StandardScaler` is used to standardize the input features before training the model.

### 10. Machine Learning Model

The project uses:

**Linear Regression**

The model is trained using the scaled training data and then used to predict Global Active Power for the test dataset.

### 11. Model Evaluation

The model is evaluated using:

* **Mean Squared Error (MSE)**
* **R² Score**

An Actual vs. Predicted scatter plot is also created to visually compare the model's predictions with the actual values.

---

## 📈 Model Evaluation

The notebook calculates:

### Mean Squared Error

MSE measures the average squared difference between actual and predicted values.

Lower MSE indicates better prediction performance.

### R² Score

R² measures how well the model explains the variation in the target variable.

A value closer to **1** generally indicates better model performance.

> The exact evaluation values are generated when the notebook is executed.

---

## 🔮 Prediction on New Data

The trained model can also make predictions for custom input values.

Example input:

```python
custom_values = [[12, 5, 240, 12, 5, 18]]
```

The values represent:

```text
hour = 12
day = 5
Voltage = 240
Sub_metering_1 = 12
Sub_metering_2 = 5
Sub_metering_3 = 18
```

The input is scaled using the same `StandardScaler`, and the trained Linear Regression model predicts the corresponding **Global Active Power**.

---

## 📁 Project Structure

```text
Household-Electric-Power-Consumption/
│
├── Household Electric Power Consumption.ipynb
└── README.md
```

If you later add the dataset to the repository, the structure can be expanded as:

```text
Household-Electric-Power-Consumption/
│
├── data/
│   └── household_power_consumption.txt
│
├── Household Electric Power Consumption.ipynb
│
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Open the notebook

```bash
jupyter notebook
```

Then open:

```text
Household Electric Power Consumption.ipynb
```

### 4. Update the dataset path

The current notebook uses a Google Colab/Google Drive path:

```python
/content/drive/MyDrive/DataSet/household_power_consumption.txt
```

If you upload the dataset to your GitHub repository, update the path accordingly.

---

## 📌 Key Learning Outcomes

Through this project, I practiced:

* Data loading and cleaning
* Handling missing values
* Date and time feature extraction
* Exploratory Data Analysis
* Data visualization
* Correlation analysis
* Feature selection
* Train-test splitting
* Feature scaling
* Linear Regression
* Model prediction
* Regression model evaluation

---

## 👨‍💻 Author

**Mozahidul Alam**

CSE & AI Student
Khulna Khan Bahadur Ahsanullah University

---

## ⭐ Future Improvements

Possible improvements for this project include:

* Comparing Linear Regression with other regression algorithms.
* Performing more advanced feature engineering.
* Using time-series-specific approaches.
* Hyperparameter tuning for alternative models.
* Comparing multiple models using the same evaluation metrics.
* Improving prediction performance through additional relevant features.
