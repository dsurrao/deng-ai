# todo
add more existing features
ratios of features
standing water estimate, rainfall
air temperature

# Overview
Notebook for the [DengAI: Predicting Disease Spread](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/) machine learning challenge.

The code assumes that the following files exist in a `data` directory:
- dengue_features_train.csv
- dengue_labels_train.csv
- dengue_features_test.csv

# Dependencies
pip3 install polars

pip install numpy==1.26.4 (newer versions of numpy generate a runtime error related to dtype)


Tips on Discovering New Features
Understand the features. Refer to your dataset's data documentation, if available.
Research the problem domain to acquire domain knowledge. If your problem is predicting house prices, do some research on real-estate for instance. Wikipedia can be a good starting point, but books and journal articles will often have the best information.
Study previous work. Solution write-ups from past Kaggle competitions are a great resource.
Use data visualization. Visualization can reveal pathologies in the distribution of a feature or complicated relationships that could be simplified. Be sure to visualize your dataset as you work through the feature engineering process.

Tips on Creating Features
It's good to keep in mind your model's own strengths and weaknesses when creating features. Here are some guidelines:
Linear models learn sums and differences naturally, but can't learn anything more complex.
Ratios seem to be difficult for most models to learn. Ratio combinations often lead to some easy performance gains.
Linear models and neural nets generally do better with normalized features. Neural nets especially need features scaled to values not too far from 0. Tree-based models (like random forests and XGBoost) can sometimes benefit from normalization, but usually much less so.
Tree models can learn to approximate almost any combination of features, but when a combination is especially important they can still benefit from having it explicitly created, especially when data is limited.
Counts are especially helpful for tree models, since these models don't have a natural way of aggregating information across many features at once.

Mosquitoes thrive in warm, humid conditions and are most active when temperatures are between 65 and 80 degrees Fahrenheit, with humidity above 70%. Hotter weather, especially when combined with humidity, can increase mosquito populations and activity. Conversely, temperatures below 50°F significantly reduce mosquito activity, and they become dormant when temperatures drop below freezing. Rainfall can also influence mosquito populations by creating breeding grounds in standing water. 

