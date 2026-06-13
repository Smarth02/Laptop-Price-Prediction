# Laptop-Price-Prediction
<p>Laptop Price Predictor using Machine Learning based on specifications like RAM, Weight, Screen Size, Company, Type, OS etc.</p>
<h2>Dataset</h2>
<p>The dataset was taken from Kaggle https://www.kaggle.com/code/nehahatti/laptop-price-prediction/input</p>
<h2>Features</h2>
<ul>
  <li>'Company' — Manufacturer (e.g., Dell, HP, Apple)  
  <li>'TypeName' — Laptop category (e.g., Gaming, Ultrabook, Notebook)
<li>'Inches' — Screen size
<li>'Ram' — RAM in GB
<li>'Weight' — Weight in kg
<li>'OpSys' — Operating system
<li>'ScreenResolution' — Display resolution
<li>'Cpu' — Processor details
<li>'Memory' — Storage configuration
<li>'Price' — Target variable (in INR/currency units)
</ul>
<h2>Workflow</h2>
<ol>
  <li><b>Data Preprocessing</b>
<ul><li>Load dataset from URL
<li>Change the datatype of columns 'Ram' and 'Weight' from strings into numbers
<li>Remove the unnamed index column
</ul>

<li><b>Exploratory Data Analysis (EDA)</b>
  <ul>
<li>Count plots for 'Company', 'TypeName', 'Ram', and 'OpSys'
<li>Box plots for outlier detection on 'Price', 'Inches', 'Ram', and 'Weight'
<li>Scatter plots showing price variation across categorical features
<li>Correlation heatmap for numerical features
  </ul>

<li><b>Outlier Removal</b>
  <ul>
<li>Cleaned data using the 1.5*IQR method on all numerical columns
  </ul>

<li><b>Feature Engineering</b>
<ul><li>One-hot encoding via 'pd.get_dummies()' on all categorical columns
</ul>
<li><b>Model Training & Evaluation</b>
Two models are trained and compared:

| Model | Notes |
|---|---|
| Random Forest Regressor | Ensemble model; handles non-linearity well |
| Linear Regression | Baseline model |

**Metrics reported:** MAE, MSE, RMSE, R² Score
</ol>
<h2>Project Structure</h2>
<p>Laptop Price Prediction/<br>
  │<br>
  ├──Laptop_Price_Prediction.ipynb # Main notebook<br>
  ├── laptop_data.csv #Dataset<br>
  └── README.md # This file<br>
</p>

<h2>Results</h2>
<p>The Random Forest Regressor generally outperforms Linear Regression on this dataset due to the non-linear relationships between laptop specs and price.</p>
