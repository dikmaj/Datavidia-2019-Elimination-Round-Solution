# Datavidia 2019 [Elimination Round] - Solution
This repository contains solution **(Python Notebook)** from team **Ednoer Squad** and data for the **Datavidia 2019 [Elimination Round]** competition 
held on the Kaggle Inclass platform.

**Kaggle Competitions Link :** https://www.kaggle.com/c/datavidia2019

`ednoer-squad-final-kernel-writeup.ipynb` contains solutions and explanations of the methods used to generate predictions in the test data. 
The explanation is written in markdown form on the notebook in **Indonesian language (Bahasa)**.

**Requirements:** \
Latest version of:
- [`Python`](https://www.python.org/) and [`Jupyter Notebook`](https://jupyter.org/)
- [`numpy`](https://numpy.org/) and [`pandas`](https://pandas.pydata.org/)
- [`scikit-learn`](https://scikit-learn.org/stable/) 
- [`xgboost`](https://xgboost.readthedocs.io/en/latest/)
- [`lightgbm`](https://lightgbm.readthedocs.io/en/latest/)
- [`catboost`](https://catboost.ai/).

This dependency is already in the Kaggle Kernel and can be used directly to run `ednoer-squad-final-kernel-writeup.ipynb`. \
**Warning:** This notebook is designed to run on a CPU. 
You can use GPU by modifying the code in the training section (model parameters `xgboost`, `lightgbm`, and `catboost`), 
provided that it **does not guarantee** the same results as on the solution notebook **(not reproducible)**.

### Data Descriptions:
- `flight.csv` - Training data containing various flight transactions and their attributes
- `test.csv` - Test data that contains flight transactions that must be predicted whether there is a cross sell or not
- `hotel.csv` - Contains hotel data and its attributes
- `Data Dictionary.pdf` - Contains variable meanings of each data
- `sample_submission.csv` - Contains a submission format to Kaggle.


**Note:** We want to predict *"whether a hotel booking transaction occurs **(cross sell)** in an airplane ticket purchase transaction"*. 
In the train data, there is a `hotel_id` column. It can be said that if `hotel_id` is `"None"` then there is no cross sell. 
Meanwhile, if the `hotel_id` value is other than that, a cross sell occurs.
