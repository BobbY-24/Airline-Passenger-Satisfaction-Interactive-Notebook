Airline Passenger Satisfaction Interactive Notebook
Project Overview
This project is an interactive Jupyter Notebook that allows users to explore and predict airline passenger satisfaction. Users can visualize trends in the dataset and input passenger details to get real-time predictions.
The notebook combines:
Exploratory Data Analysis (EDA) with interactive plots.


Machine Learning for predicting passenger satisfaction.


Interactive Widgets using ipywidgets for dynamic input.



Dataset
Source: Kaggle – Airline Passenger Satisfaction


Description: Dataset includes passenger demographics, flight info, and service ratings.


Key Columns:
 Age, Flight Distance, Customer Type, Type of Travel, Class, Inflight wifi service, Seat comfort, Food and drink, Inflight entertainment, Gate location, Baggage handling, Online boarding, Leg room service, Ease of Online booking, On-board service, Checkin service, Cleanliness, Inflight service, Departure/Arrival time convenient, Gender, satisfaction



Features
1. Interactive Data Visualization
Select a categorical feature from a dropdown to see satisfaction counts.


Select a numeric feature from a dropdown to see histograms of satisfaction distribution.


Uses Plotly for dynamic plots that can be zoomed, hovered, and filtered.


2. Model Training
Trains a Random Forest Classifier on 80% of the dataset.


Preprocessing includes:


One-hot encoding for categorical features.


Passthrough for numeric features.


Displays classification report and confusion matrix for model evaluation.


3. Interactive Prediction
Users can adjust sliders for numeric features and dropdowns for categorical features.


Predicts if a passenger is satisfied or dissatisfied.


Immediate visual feedback for predictions.



Installation
Clone the repository:


git clone <your-repo-url>
cd <repo-folder>

Create a virtual environment and install dependencies:


conda create -n airline_env python=3.10
conda activate airline_env
pip install -r requirements.txt

Launch the notebook:


jupyter notebook Airline_Satisfaction_Interactive.ipynb


Dependencies
Python 3.10+


pandas


numpy


matplotlib


seaborn


plotly


ipywidgets


scikit-learn



Usage
Open the notebook in Jupyter or JupyterLab.


Run cells in order:


Load and clean the dataset.


Explore the data with interactive plots.


Train the Random Forest model.


Use interactive sliders/dropdowns to predict new passenger satisfaction.



Example Prediction
Input passenger details:
Age: 35


Flight Distance: 1200


Inflight Wifi Service: 4


Seat Comfort: 5


Customer Type: Loyal


Class: Economy


Prediction: 😊 Satisfied

