# Network Security System using ML, Github Actions, Dagshub, MLFlow and Docker

## Overview
- This is a phising dataset having features such as 'having_IP_addres', 'URL Length', 'Favicon', 'Port', etc. This was downloaded from web and was pushed into MongoDb Atlas which was used for ingestion into pipeline at later stage

- The dataset has more than 11000 records has about 20+ features.

## Motivation
- This problem deadls with cybersecurity which is a necessity in today's generation.

- I tried to implement ML into this domain

## Methodology

### EDA (Exploratory Data Analysis)
- I have plotted various graphs to visualize the data. Some of them are as follows : 

![PriceVsAirline](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/AirlineVsPrice.png)
![PriceVsDest](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/DestinationVsPrice.png)
![PriceVsSource](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/SourceVsPrice.png)
![PriceVsStops](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/StopsVsPrice.png)

- Required Graphs are plotted using seaborn,matplotlib libraries.

- Also heatmap is plotted for checking the corelation between target and predictor variables.
![Heatmap](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/heatmap.png)

### Feature Engineering
- I have derived many useful features from existing features so that I can use them in my model. You can check the notebook attached.

- I have handled categorical variables i.e nominal ar well as ordinal by using one-hot-encoding and label encoding whereever necessary.

### Feature Selection
- I have used ExtraTreesRegressor for checking feature importances.

- I have also used barplot for visualising them:
![Feature_Imp](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/readme_resources/feature%20importances.png)

### Model Making

- I have built a RandomForestRegressor model with default hyperparameters initially.

- I chose this model just because I thought ensemble model would work better. But you can try different models too.

### Hyper-Parameter Tuning

- I have tuned the hyperparameters 'n_estimators', 'max_depth', 'max_features' by using RandomisedSearchCV. I used  this because this works faster than GridSearchCV.

- I again built a RF model with best hyper-parameters selected from CV.

### Metrics

- I have used 'r2_score' as my metric here. You can use any different metric for regression.

- Further I have plotted and checked error terms also to check whether they are normally distributed around 0.

### DATA SOURCE
- [Flight Fare Dataset](https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh/)

### Notebook
- [Flight Fare Predictor](https://github.com/Pratik872/ML/blob/main/E2E%20Project/FlightFarePredictor/Flight%20Fare%20Prediction.ipynb)

### Built with 🛠️
- Packages/Repo : Pandas,Numpy,Seaborn,Matplotlib,Sklearn,Flask,Pickle,Git

- Dataset : Kaggle

- Coded on : Jupter Notebook (modelling), VSCode(building application)

### Deployment
- Deployed using Heroku(PAAS)

- For deployment repository click [here](https://github.com/Pratik872/ML/tree/deployFlight)

- For Web Application click [here](https://flight-fare-deploy.herokuapp.com/)
