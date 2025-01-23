# Machine Downtime Prediction API

## Overview
This project involves training a machine learning model to predict machine downtime using manufacturing data and setting up a Flask API to serve the model. The trained model is a Random Forest Classifier that uses features such as air temperature, process temperature, rotational speed, torque, and tool wear to make predictions.
## Requirements
- Python 3.6 or higher
- Flask
- Pandas
- Scikit-learn
- Numpy
- Joblib
## Installation

## 1. **Clone the repository:**
```
git clone <repository-url>
cd <repository-folder>
```

#### Install the required Python packages:
```
pip install numpy pandas scikit-learn joblib flask
```
## Dataset
The dataset ai4i2020.csv contains manufacturing data with the following features:
- Air temperature [K]
- Process temperature [K]
- Rotational speed [rpm]
- Torque [Nm]
- Tool wear [min]
- Machine failure (target variable)

## Model Training
1. Load the dataset and select features and target.
2. Split the data into training and testing datasets.
3. Train a Random Forest Classifier model.
4. Save the trained model to a file.

## API Setup
1. Set up a Flask API with endpoints for health check, model information, and making predictions.
2. Load the trained model and create endpoints to interact with it.
3. Running the API
## 2. To run the API, use the following command:
```
python app.py
```
Access the API: The application will be available at `http://127.0.0.1:5000` by default.


## 3. **Once the API is running, you can access the following endpoints:**
 - / - Welcome message for the API

 - /health - API health check

 - /info - Model or dataset information

 - /predict - Predict machine downtime (POST request with JSON input)

## 3. **Example JSON Input for Prediction**
   ```
   {
        "Air temperature [K]": 300,
        "Process temperature [K]": 310,
        "Rotational speed [rpm]": 1500,
        "Torque [Nm]": 40,
        "Tool wear [min]": 100
    
   }
   ```
   
  
