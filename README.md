# Census-Prediction

Predicting the person's income to see if he/she is making more than $50K or not. Considering different countries and their currencies with the person's age, education, his/her workclass, his/her marrital status, occupation, the amout of time he/she works etc.

## Tech Stack:
* Front-End:HTML, CSS
* Back-End:Flask
* IDE:Jupyter Notebook, Visual Studio Code

## How to run this app:
* First create a virtual environment by using this command: conda create -n myenv python=3.6
* Activate the environment using the below command: conda activate myenv
* Then install all the packages by using the following command: pip install -r requirements.txt
* Now for the final step. Run the app
* python app.py

## Data Preprocessing:
* Categorical columns like Fuel_Type, Owner, Seller_Type, Transmission has been imputed using the mapping method.
* Numerical columns such as Present_Price, Kms_Driven has high skewness and they has been transformed using numpy.log1p for better use of the column.
* Tree based models doesn't need transformation(min_max_scalar/standard_scalar/robust_scalar), so I avoided it completely.

## Model Creation:
* Different types of models were tried like catboost, random forest, logistic regression, xgboost, lightgbm.
* Out of these catboost, xgboost and lgbm were top 3.
* The conclusion were made using classification metrics **roc curve and auc score**
## Model Deployment:
The model is deployed using Flask at Heroku server at https://ensus-prediction.herokuapp.com/.

## Screenshots:

### Front page:
![front_page](https://user-images.githubusercontent.com/15306703/146351267-90c0c4bf-c598-4ff5-9d69-75afe357c73b.png)

### Prediction 1:
#### Predicting page:
![less_than_50k_predicting](https://user-images.githubusercontent.com/15306703/146352382-fb68cb5a-2d62-4d61-8769-5993a31f2876.png)

#### Prediction:
![less_than_50k](https://user-images.githubusercontent.com/15306703/146351677-7ed4389f-3882-40c4-bb3e-dc1aeac80451.png)

### Prediction 2:
#### Predicting page:
![more_than_50k_predicting](https://user-images.githubusercontent.com/15306703/146352461-6a4aa403-75fb-493c-ada8-854843b2958b.png)

#### Prediction:
![more_than_50k](https://user-images.githubusercontent.com/15306703/146352508-90330889-8364-4bef-b1bd-ca12b17d9bc6.png)
