**Delivery Time Prediction using Machine Learning**

Predicting food delivery time using data preprocessing, feature engineering, and machine learning models.

---

**Dataset Overview**

The dataset contains 197,428 rows and 14 columns, including order details, store information, partner availability, and timestamps.
After preprocessing and feature engineering, it was expanded to 95 features.

---

**Project Workflow**

**Data Loading**
Dataset loaded using Pandas with initial exploration.

**Feature Engineering**
Extracted time-based features:

* created_hour
* created_day_of_week
* created_month

Computed:

* delivery_time_minutes

**Data Cleaning**

* Removed missing values in key columns
* Filled missing categories with "unknown"
* Dropped unnecessary columns
* Encoded store IDs

**Exploratory Data Analysis**

* Correlation heatmap
* Boxplot for outlier detection
* Identified correlated features

**Outlier Removal**
Used IQR method to remove extreme values outside the normal delivery range.

**Feature Encoding**
One-hot encoding applied to categorical variables.

**Train-Test Split**
80 percent training and 20 percent testing.

---

**Models Used**

* Linear Regression
* Random Forest Regressor
* XGBoost Regressor

---

**Model Performance**

Linear Regression
MAE: 10.79
RMSE: 13.56

Random Forest
MAE: 10.27
RMSE: 12.96

XGBoost
MAE: 10.11
RMSE: 12.77

---

**Tech Stack**

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
XGBoost

---

**Accessing Dataset (Google Colab)**

```python
from google.colab import drive
drive.mount('/content/drive')
```

```python
import pandas as pd
data = pd.read_csv('/content/drive/MyDrive/dataset.csv')
```

Note: This step is only required for Google Colab.
For local execution, place the dataset in the project folder.

---

**How to Run**

**Run Locally**

```bash
git clone https://github.com/nachiketh906/delivery-time-prediction.git
cd delivery-time-prediction
pip install -r requirements.txt
```

Place dataset.csv in the project directory.

**Run on Google Colab**

Upload dataset to Google Drive
Use the mounting code above
Run the notebook
