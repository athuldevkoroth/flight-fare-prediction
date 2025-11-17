# ✈️Flight Fare Prediction – Machine Learning Project

This project predicts flight ticket prices based on various travel features such as airline, source, destination, duration, stops, and more.
It includes the complete notebook, trained model, dataset, and requirements to reproduce the results.

## 📂 Project Structure
```
├── FlightFare.ipynb        # Jupyter Notebook (full EDA + model building)
├── dataset.csv             # Training dataset
├── requirements.txt        # Required Python libraries
├── model.zip               # Zipped trained model (.pkl inside)
└── README.md               # Project documentation
```


## 🧠 What This Project Includes

- Exploratory Data Analysis (EDA)
- Data cleaning & preprocessing
- Duration cleaning
- Scaling of numerical data
- Feature engineering
- Model training (RandomForest / DecisionTree)
- Hyperparameter tuning
- Model evaluation & metrics
- Exported trained model (model.pkl inside model.zip)

- # 📊 Project Analysis Report

## 1. Introduction
Flight prices vary drastically based on airline, route, demand, season, duration, and number of stops.  
The goal of this project is to build a machine learning model that can accurately predict flight prices.

---

## 2. Dataset Overview

### Key Features
- Airline  
- Source & Destination  
- Date_of_Journey  
- Dep_Time / Arrival_Time  
- Duration  
- Total_Stops  
- Additional_Info  

**Target variable:** Price  

**Price Range:**  
- Minimum: ₹1759  
- Maximum: ₹79,512  

---

## 3. Exploratory Data Analysis (EDA)

### Key Insights
- Prices differ significantly between airlines.  
- More stops usually reduce the price.  
- Duration is strongly correlated with price.  
- Peak departure and arrival hours influence cost.  
- `Additional_Info` is mostly “No info” and less useful.

---

## 4. Data Preprocessing

### ✓ Date & Time Extraction
- Journey Day  
- Journey Month  
- Dep Hour & Minute  
- Arrival Hour & Minute  

### ✓ Duration Cleaning
Split into:
- Duration Hours  
- Duration Minutes  

### ✓ Categorical Encoding
- Airline, Source, Destination → OneHotEncoding  
- Total_Stops → numeric mapping  

### ✓ Feature Scaling
- StandardScaler for numerical values  

---

## 5. Model Building

### Models Tested
- RandomForestRegressor  
- DecisionTreeRegressor  
- Gradient Boosting  
- Linear Regression (baseline)  

**Best Performing Model:** Random Forest  
*(Some overfitting expected but test performance is strong.)*

---

## 6. Model Evaluation

### Metrics Used
- R² Score  
- Mean Absolute Error (MAE)  
- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  

### Results Summary
- High training accuracy  
- Good generalization on test data  
- Slight overfitting (typical for tree-based models)

---

## 7. Feature Importance (Top Contributors)

Most influential features (in order):

1. Total_Stops  
2. Duration Hours  
3. Airline  
4. Source  
5. Destination  
6. Journey Month  
7. Departure Time  

These match real-world ticket pricing logic.

---

## 8. Exported Model & Deployment Prep

The trained model is exported as:



## 📦 Requirements

This project uses only a few basic Python libraries:

- pandas  
- numpy  
- seaborn  
- matplotlib  
- scikit-learn  

All dependencies are listed in **requirements.txt**.

## 📦 Model File (.zip)

GitHub doesn’t allow uploading files larger than 25 MB directly.
So the model is compressed into model.zip — unzip it to get model.pkl.

## 🔮 Future Plans

- Convert this into a web application (Flask / FastAPI + HTML/CSS + JS)
- Add a proper preprocessing script for production use
- Build a UI for fare prediction

## 📧 Contact

Feel free to connect with me on LinkedIn or reach out if you want to collaborate or review the project.

