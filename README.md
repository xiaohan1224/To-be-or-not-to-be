To be, or not to be
=============
Shakespeare Dataset Classification
=============
Resource: https://www.kaggle.com/kingburrito666/shakespeare-plays
Since there aren't many features in the raw file, and PlayerLine and Play are in English language, so encode PlayerLine and Play needs to be encoded.

Main steps:
    1. Data cleaning: All rows contain null are removed, since they are just voiceover
    2. Data Transformation:
                                        a) ActSceneLine is seperated to 3 columns: Act, Scene and Line
                                        b) Label Encoder is used to transform target labels with value between 0 and
                                            n_classes -1
                                        c) One hot is used to transform categorical features as a one-hot numeric array
    3. Feature correlation
    4. Decision tree, Random Forest and Logistic Regression classifiers are applied

Result:
    1. Random Forest Classifier accuracy: 55.84%
    2. Decision Tree Classifier accuracy: 54.88%
    3. Logistic Regression Classifier accuracy: 25.27%
From the result, Random Forest Classifier with current parameter setting, overperfomrs Decisoin tree classifier and Logistic Regression Classifier.

==============
.
├── notebooks
    ├── To be, or not to be
    └── correlation.png
├── README.md
└── data
    ├── Shakespeare_data.csv
    ├── alllines.txt
    └── william-shakespeare-black-silhouette.jpg
