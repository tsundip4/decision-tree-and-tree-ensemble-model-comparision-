Overview: This project demonstrates a comparative analysis of three popular machine learning algorithms—Decision Tree, Random Forest, and XGBoost—applied to a heart disease classification dataset. The goal is to evaluate model performance across different hyperparameter(depth/nestimators) and visualize results for interpretation


Datsets Source: Source: Kaggle Heart Disease Dataset (heart.csv) Target Variable: Heart Disease (binary: 0 = No, 1 = Yes)


Model implemented: This notebook implements and compares three machine learning models: Decision Tree, Random Forest, and XGBoost. For the Decision Tree Classifier, we tested max_depth values of [2, 3, 4, 6, 8, 10, 12]to find the optimal depth that balances performance without overfitting. The best validation and test performance was achieved at depth 3, beyond which the model begins to overfit. The Random Forest Classifier was configured with n_estimators=100 and the same depth range. It performed best at max_depth=10, showing underfitting at lower depths and overfitting at depth 12. For XgBoost, we simply used the n_estimator of 100 and stopping rounds of 10 to stop the model if it goes without improvement for the next 10 rounds.


Performance Visualization Training vs Validation Scores plotted for both Decision Tree and Random Forest across different depths. Key Insight: Random Forest achieved the highest accuracy among all models across most depth settings, outperforming XGBoost on this dataset. This suggests that bagging-based ensembles were better suited for the data distribution and feature interactions than boosting-based methods.


How to run: Upload the heart.csv file to sample_data/ in Colab or adjust path.
Execute cells sequentially. 
Modify hyperparameters in max_depth_list to experiment further.





