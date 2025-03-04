# Flood Prediction and Route Rerouting using LSTM and Google Maps API

## Project Overview
This project aims to predict flood conditions in Bangalore using historical rainfall and weather data to detect flooded areas. We are using Long Short-Term Memory (LSTM) deep learning models to predict the likelihood of flooding based on various parameters like rainfall intensity, temperature, humidity, atmospheric pressure, river level, and drainage system condition. The model is trained on a dataset that includes geographic coordinates, weather conditions, and flood status, with the goal of forecasting potential flood events.

In addition to flood prediction, this project integrates the Google Maps API to monitor traffic routes and automatically reroute vehicles in real-time if a flooding condition is detected along the intended path. This system helps in ensuring safe travel by advising alternate routes during flood conditions.

## Key Features
- **Flood Prediction using LSTM:** Predict flooding events based on various weather and infrastructure parameters like rainfall intensity, river levels, population density, and more.
- **Google Maps API Integration:** Use coordinates to monitor and update routes in real-time. If a flood is predicted, the system reroutes navigation to avoid flooded areas.
- **Data Preprocessing:** Clean and normalize data before feeding it into the model. Includes handling missing values, encoding categorical variables, and normalizing continuous features.
- **Real-time Flood Monitoring:** Continuously check geographic coordinates and provide flood status updates for different regions of Bangalore.

## Steps for Preprocessing

1. **Data Cleaning:**
   - Handle missing or inconsistent data points.
   - Remove or impute any rows with missing values.

2. **Feature Engineering:**
   - Extract features from coordinates (latitude, longitude) and weather data (rainfall, temperature, humidity, etc.).
   - Encode categorical variables (e.g., drainage system condition, urbanization level) using one-hot encoding or label encoding.

3. **Normalization:**
   - Scale numerical values like rainfall intensity, temperature, and river level to bring all features to a similar range (e.g., using Min-Max scaling or StandardScaler).

4. **Train-Test Split:**
   - Split the data into training and testing sets (typically 80-20 or 70-30).

5. **LSTM Model Design:**
   - Build an LSTM model with layers such as embedding, LSTM layers, dropout for regularization, and a dense output layer for flood prediction (binary classification: flooded vs. not flooded).

6. **Model Training:**
   - Train the model on the preprocessed data and evaluate its performance using metrics like accuracy, precision, recall, and F1 score.

7. **Google Maps API Integration:**
   - Use the model's predictions to check routes in real-time, based on user input coordinates, and reroute traffic if floods are detected.

## Technologies Used
- **Deep Learning:** LSTM (Long Short-Term Memory) for time-series prediction.
- **Google Maps API:** For real-time navigation updates based on flooding data.
- **Python Libraries:** Pandas, NumPy, TensorFlow/Keras, scikit-learn, Matplotlib.

## Setup Instructions
1. Clone the repository.
2. Install the necessary libraries with:
   ```bash
   pip install -r requirements.txt
