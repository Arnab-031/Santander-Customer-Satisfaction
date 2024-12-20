# Santander-Customer-Satisfaction
# Overview
Customer satisfaction is a vital metric for success across all levels, from support teams to executives. Dissatisfied customers often leave silently, without expressing their concerns. Santander Bank challenges Kagglers to predict dissatisfied customers early, enabling proactive actions to enhance their experience and prevent churn. In this project, I analyzed hundreds of anonymized features to determine whether customers were satisfied or dissatisfied with their banking experience.
The uploaded Jupyter Notebook analyzes customer satisfaction using machine learning models, primarily Decision Trees. Below is an analysis of the key features, technologies used, and key insights:

# Key Features
1.	Data Preparation:
Dropped irrelevant columns (ID) and separated the target variable (TARGET).
Split data into training and validation sets.
2.	Exploratory Data Analysis (EDA):
Visualized distribution relationships (e.g., num_var22_ult3 by TARGET).
3.	Model Training and Evaluation:
Implemented multiple Decision Tree models:
Baseline Model.
Depth-limited model (max_depth=5).
Entropy criterion model.
Limited leaf nodes (max_leaf_nodes=10).
Evaluated models using ROC AUC scores.
4.	Custom Model Evaluation:
Defined a reusable function to train models and evaluate AUC.
5.	Final Predictions:
Used the best-performing model (max_depth=5) for test predictions.
Prepared a submission file.

# Technologies Used
1.	Programming Language:
Python.
2.	Data Manipulation and Analysis:
Libraries: pandas, numpy.
3.	Visualization:
Library: seaborn, matplotlib.
4.	Machine Learning:
Models: DecisionTreeClassifier from sklearn.
Evaluation Metric: roc_auc_score.
# Dataset
https://www.kaggle.com/c/santander-customer-satisfaction/data

# Key Insights
1.	Decision Tree with limited depth (max_depth=5) achieved the highest ROC AUC (0.8183), outperforming the baseline (0.5747).
2.	EDA revealed significant differences in transaction counts over the last three months (num_var22_ult3) between satisfied and unsatisfied customers.
3.	Limiting the complexity of the model (e.g., max_depth, max_leaf_nodes) improves predictive performance by preventing overfitting.
4.	Using entropy as the splitting criterion did not improve model performance compared to the Gini index.
5.	The structured evaluation pipeline ensures reproducibility and ease of comparison across models.

￼
