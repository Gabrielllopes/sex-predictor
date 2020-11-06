Sex Predictor
==============================

This projects follows the cookiecutter data science project template.

After the Project Organization section there is a 'Logs' section where I describe my decisions towards this project.

Project Organization
------------
 
    ├── README.md          <- The top-level README for developers using this project.  
    ├── data  
    │   ├── processed      <- The final, canonical data sets for modeling.  
    │   └── raw            <- The original, immutable data dump.  
    |  
    ├── models             <- Trained and serialized models.  
    │  
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.  
    │  
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.  
    │  
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`  
    │  
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported  
    ├── src                <- Source code for use in this project.  
    │   │  
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling or prediction
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions

## Logs

### Log 0.0 - before starting
After reading the file `references/technical_test_datascientist.md`
and giving a little look at the data `data/raw/test_data_CANDIDATE.csv`
the following things come to my mind.  
* I need to stablish a baseline metric (the porcentage of male/female shoud be enough).
* There is some missing data, this should be treated.
    - The column 'cp' has the same values to all the samples, It can be ignored.
* There not a lot of that, deep learnign models would not be a good fit, so I will explore shallow models.
* There is not a lot of that cross validation is a good option because:
    - Training will not be timing consiming.
    - There is not enough data to split the dataset in a non bias way.
obs: (I am keeping track of the data with git because it's small. Otherwise I woud rather use DVC)

### Log 0.1 - After finishing the first data analisys
The data analissy was performed in the `/notebooks/data-analisys.ipynb` were I explaned each feature
and clean the data for modeling.
I also had some insights that I explained in the notebook.  
If this was a regular project I would done the feature engineerig part in a python script located in `src/features/build_features.py`
This would make easyer of reuses that code to engeneer more data.

### Log 0.2 - Modeling
The modeling part was performed in the `/src/models/find-models.ipynp` 
The best model was saved in `/models/model.pickle.dat`
The explanation why I choose xgbost and the other techiniques was explained in the nootebook



--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
