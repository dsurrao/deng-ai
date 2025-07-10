# Overview
Notebook for the [DengAI: Predicting Disease Spread](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/) machine learning challenge.

The code assumes that the following files exist in a `data` directory:
- dengue_features_train.csv
- dengue_labels_train.csv
- dengue_features_test.csv

# Dependencies
pip3 install polars

pip install numpy==1.26.4 (newer versions of numpy generate a runtime error related to dtype)