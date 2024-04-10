# Firm's-bankruptcy-prediction
# Problem
Firm collapse prediction has been a subject of interest for almost a century and it still ranks high among the hottest topics in economics. The aim of predicting financial distress is to develop a predictive model that combines various econometric measures and allows one to foresee a financial condition of a firm. The purpose of bankruptcy prediction is to assess the financial condition of a company and its future perspectives within the context of longterm operation on the market.

# Methodology Overview:
# 1.Data Preparation:

The dataset includes attributes like net profit, total liabilities, working capital, and many others, alongside a binary response variable indicating bankruptcy status. Missing values are imputed with the median of each column. Outliers are identified and removed based on z-scores. The dataset is split into training and testing sets, with upsampling applied to the training set to address class imbalance using SMOTE.

# Feature Selection:

After initial data cleaning and preparation, a boxplot visualization and a histogram of the response variable are used to understand the distribution of features and the class imbalance. A feature selection step is included to identify and focus on the most relevant features for the prediction task.

# Model Training and Selection:

Several machine learning models are trained and evaluated, including Gaussian Naive Bayes, Logistic Regression, Support Vector Machine (SVM), and Gradient Boosting Machine (GBM). Each model is trained using a pipeline that includes preprocessing steps such as polynomial feature creation, scaling, and feature selection through percentile selection. GridSearchCV is utilized for hyperparameter tuning to optimize model performance based on recall score.

# Model Evaluation:

Models are evaluated using a set of metrics including accuracy, precision, recall, F1 score, and macro-averaged F1 score. A comparison report is generated to summarize the performance of each model on the test dataset. The ROC curve is plotted for selected models to visualize their performance in terms of the trade-off between true positive rate and false positive rate.

# Application of the Best Model:

The best-performing model, based on the evaluation metrics, is selected for making predictions on new samples. Probabilities of bankruptcy are computed for new samples using the selected GBM model. These probabilities are appended to the new samples dataset, and the results are saved to a CSV file, providing a practical output for further analysis or decision-making.

# Key Takeaways:

The code demonstrates a comprehensive approach to bankruptcy prediction, leveraging statistical techniques for data preprocessing, sophisticated machine learning models for prediction, and detailed model evaluation to ensure the selection of the most effective model. It highlights the importance of addressing class imbalance in datasets, the usefulness of hyperparameter tuning in optimizing model performance, and the practical application of machine learning models to generate actionable insights.
