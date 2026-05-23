# Airline Passenger Satisfaction Interactive Notebook

## Overview
This project is an interactive Jupyter Notebook for exploring and predicting airline passenger satisfaction. It combines exploratory data analysis, Plotly visualizations, a Random Forest classifier, and `ipywidgets` controls for experimenting with passenger profiles. The emphasis is on making a tabular ML workflow interactive and understandable.

## Motivation
Interactive notebooks are useful for communicating machine learning results to nontechnical audiences. This project shows how EDA, model evaluation, and prediction interfaces can be combined in one reproducible notebook. It also complements the separate airline satisfaction modeling repo by focusing more on user interaction and exploratory analysis.

## Dataset
- **Source:** Kaggle Airline Passenger Satisfaction dataset.
- **File:** `data/airline_satisfaction.csv`
- **Size:** 25,976 passenger records.
- **Target variable:** `satisfaction`.
- **Important features:** passenger demographics, customer type, type of travel, flight distance, cabin class, delay times, and service ratings such as online boarding, seat comfort, inflight entertainment, cleanliness, and baggage handling.
- **Known limitations:** The dataset is static, public, and benchmark-like. It may not reflect current airline operations, sampling bias, or differences across airlines and regions.

## Methods
- Loaded and inspected the airline satisfaction dataset.
- Built interactive categorical and numeric visualizations with Plotly and `ipywidgets`.
- Preprocessed categorical variables with one-hot encoding.
- Trained a Random Forest classifier on an 80/20 train/test split.
- Evaluated the classifier with precision, recall, F1-score, and support.
- Added widget-based controls for testing passenger profiles.

## Results
The notebook reports approximately **96% test accuracy** for the Random Forest classifier.

Classification report from the notebook:

| Class | Precision | Recall | F1-score | Support |
| --- | ---: | ---: | ---: | ---: |
| `0` | 0.95 | 0.97 | 0.96 | 2890 |
| `1` | 0.97 | 0.94 | 0.95 | 2289 |

## Key Insights
- Interactive controls make model behavior easier to inspect than static notebook outputs alone.
- Passenger satisfaction is strongly associated with service quality ratings and travel context.
- The Random Forest model performs well on both target classes in the reported split.
- This notebook is useful as a communication artifact, not just a modeling artifact.

## Limitations
- The widget prediction interface is exploratory and should not be treated as a deployed application.
- The notebook does not yet include cross-validation or hyperparameter tuning.
- The project does not analyze subgroup robustness or fairness.
- The model may learn patterns specific to this dataset rather than general airline satisfaction dynamics.

## Future Improvements
- Add feature importance and partial dependence plots.
- Compare model predictions across passenger subgroups.
- Convert the interactive workflow into a small Streamlit app.
- Add cross-validation and saved model artifacts.
- Add a short technical note comparing this interactive notebook with the modeling-only repo.

## How to Run
```bash
git clone https://github.com/BobbY-24/Airline-Passenger-Satisfaction-Interactive-Notebook.git
cd Airline-Passenger-Satisfaction-Interactive-Notebook
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
pip install -r requirements.txt
jupyter notebook notebooks/airline_passenger_satisfaction_interactive.ipynb
```

Run the notebook cells from top to bottom. The notebook expects the dataset at `data/airline_satisfaction.csv`.
