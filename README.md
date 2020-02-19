# Disaster Response Pipeline Project

# Disaster Response Pipeline Project
## Introduction
This project was done as a requirement for the Data Scientist Nanodegree and the data was provided by Figure Eight The initial dataset contains pre-labeled tweets and messages from real-life disasters. The goal of the project is to build a Natural Language Processing tool that categorizes messages.

The Project is divided into the following parts:

1- Data processing: ETL pipeline to extract data from the source, clean data and save them in a database

2- Build a machine learning pipeline to train a model able to classify text message in categories

3- Build a web App to show model results in real-time


## Content
- 1- Data:

    - **process_data.py:** reads in the data, cleans and stores it in a SQL database. Basic usage is python process_data.py MESSAGES_DATA CATEGORIES_DATA NAME_FOR_DATABASE
  - **disaster_categories.csv** and **disaster_messages.csv**  (dataset)
DisasterResponse.db: created a database from transformed and cleaned data.
- 2- Models:

  - **train_classifier.py**: includes the code necessary to load data, transform it using natural language processing, run a machine learning model using GridSearchCV and train it. Basic usage is python train_classifier.py DATABASE_DIRECTORY SAVENAME_FOR_MODEL
- 3-  App: 
  - **run.py**: Flask app and the user interface used to predict results and display them.
templates: a folder containing the html templates

## Installation 
- Python 3.6.8 was used
- Machine learning libraries are: NumPy, SciPy, Pandas, Sciki-Learn
- Natural Language Processing library: nltk
- SQLlite Database Libraries: SQLalchemy
- Web app I used Flask and for visuals, I used plotly

## Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/



## Acknolewdgment 
Thanks for Udacity for the started code and for Figure Eight for the data