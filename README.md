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

<img width="884" height="508" alt="Screenshot 2025-08-28 at 4 59 20 PM" src="https://github.com/user-attachments/assets/c0370f3f-7495-450c-ae54-71b1add57ca5" />
<img width="231" height="365" alt="Screenshot 2025-08-28 at 4 59 24 PM" src="https://github.com/user-attachments/assets/bfa35058-9360-42bb-b6e9-2415b069842f" />
<img width="549" height="594" alt="Screenshot 2025-08-28 at 4 59 33 PM" src="https://github.com/user-attachments/assets/f6c7ec73-e737-45c9-be30-50f387b6e2be" />
<img width="402" height="424" alt="Screenshot 2025-08-28 at 4 59 39 PM" src="https://github.com/user-attachments/assets/7f49a683-c2a3-44e4-a21a-9198aae11c5c" />


Class: Economy


Prediction: 😊 Satisfied

