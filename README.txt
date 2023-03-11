Disaster Response Project

Technologies used:
- Python 3.6
- HTML
- Flask
- Plotly
- Python Packages:
  - Machine Learning libraries such as NumPy, SciPy, Pandas, Sciki-Learn
  - XGBoost
  - Python oversampling package such as imblearn
  - Regular expression operation python package such as re
  - Json
  - Natural Language Process libraries such as NLTK
  - SQLlite Database libraries such as SQLalchemy
  
The objective of this project is to analyze disaster data to build a model that classify disaster messages.



  
 File Descriptions
- ETL Pipeline Preparation.ipynb: 

  The file for data prepration which include:

      - Loads the messages and categories datasets
      - Merges the two datasets
      - Cleans the data
      - Stores it in a SQLite database
- ML Pipeline Preparation.ipynb:

  This is the machine learning file that do the following:
    - Loads data from the SQLite database
    - Splits the dataset into training and test sets
    - Builds a text processing and machine learning pipeline
    - Trains and tunes a model using GridSearchCV
    - Outputs results on the test set
    - Exports the final model as a pickle file
  

- process_data.py:

  is python file for final cleaning code from the final ETL script.
  
- train_classifier.py:

  This python file to include final machine learning code after completing the ML Pipeline.
  
Folder Descriptions
  - Data: 
  
    This folder contains messages and categories datasets in csv format and SQLite database created from the ETL Pipeline Preparation notebook.
 
 - ML Model:
 
    This folder contains all the ETL and Machine learning process.
 
 - app:
 
    This folder contains all the files necessary to run and render the web app.
  
how to execute the program:

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/messages.csv data/categories.csv data/Disaster_messages.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/Disaster_messages.db models/classifier.pkl`

2. Run the following command in the app's directory to run web app.
    `python run.py`

3.  Click the `PREVIEW` button to open the homepage or Go to http://0.0.0.0:5000/ or http://localhost:5000/

