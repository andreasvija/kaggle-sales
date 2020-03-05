# Kaggle competition solution

Notebooks of my solution for the [Predict Future Sales](https://www.kaggle.com/c/competitive-data-science-predict-future-sales) Kaggle competition, including data cleaning, data exploration, extensive feature generation, trying out different subsets of data, training models, tuning models and ensembling models. 

My best submission recieved a RMSE of 1.01247, placing me in the top 45% at the time of submission. As my training RMSE was ~0.70 and validation RMSE ~0.77, it is clear that I managed to slightly leak the target in the features I created, causing worse performance on genuinely new data, but I haven't found the source of the leakage yet.

My best submission ended up being a collection of six models: XGBoost, sklearn Gradient Boosted Trees and sklearn Random Forest, each trained on two different subsets of features - a collection of all the features that proved useful and the same collection minus many of the most heavily relied-upon features. These models' predictions were joined together using another XGBoost model. 
