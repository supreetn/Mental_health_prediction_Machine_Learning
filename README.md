# Mental_health_prediction
Mental health prediction and music recommendation system using ML

# Background and Motivation
- We all listen to music - different types for different moods
- Approximately 2 million people in United States have seeked music therapy in 2020.
- According to the American Music Therapy Association, research shows music therapy can be used to help:
  Improve overall physical rehabilitation
  Increase motivation to engage in treatment
  Alzheimer's disease and other aging-related conditions
  Acute and chronic pain, including mothers in labor
- Music causes the brain to release dopamine, a chemical which works to regulate motivation and goal-oriented behaviour.
# Datasets
We have used survey dataset to obtain users perception on music and how they respond to each musiv genre. We collected music data manually by making a list of music genres of the survey dataset and obtained corresponding songs in it. 
# Methodology

# Model Development
- We have cleaned and preprocessed the data filtering missing values, balanced the data using SMOTE.
- K-fold cross validation - we used K-fold cross-validation technique to evaluate the performance of our Random Forest classifier.
- Hyper parameter tuning - Used GridSearchCV and a 7-fold cross-validation to evaluate the performance of the model for each set of hyperparameters.

# Machine Learning Models

- Used **Random Forest** to predict the classes of music effects, for a  mental health condition if all the music features considered are improving the condition or not.
The algorithm works by randomly selecting a subset of features and a subset of data samples to build each decision tree. This process is repeated multiple times to create a forest of decision trees.
The algorithm takes the majority vote of the predictions made by all the decision trees to generate a final prediction.
Used to predict the music effects - Improved, Worsen or has No effect at all!
- **K-Nearest Neighbors (KNN)** - 
KNN was used as a machine learning model to predict the effects of music on human emotions.
Used ideal value of K = 3 for training the model.
- **Decision Tree** - DT classifier to predict favorite music genres from music features and mental health condition.
Considering all frequencies for each music genre - How much each genre is listened by people in the survey data? Never, Rarely, Sometimes, Very Frequently.
Music effects on mental health such as Improved, Worsened or has No effect at all.
DT are useful as they can handle categorical as well as numerical data, can handle inter-dependencies between features that affect the outcome.
- **Extreme Gradient Boosting** - **XGBoost** is powerful algorithm for building models with large datasets as well as with many features and can handle non-linear relationships between the features and outcomes.
Boosting trees makes it more effective than DT or RF with improved accuracy, preventing overfitting and faster processing.
Once the preferred genre is predicted, the recommended songs which has improved effect on mental health are selected from the integrated songs data.
- **Naive Bayes** - Uses Bayes' theorem. The "naive" assumption, which underlies this technique, states that each aspect of the input data is independent of every other feature. 
Effective in text categorization, spam filtering, sentiment analysis, classification tasks, particularly with high-dimensional data 
Predicts the class with the highest posterior probability by first applying Bayes' theorem to calculate the probabilities of each class given the input data.

 # Evaluation

 We observed that Random Forest was best in predicting the music effects on each issues users had. And, XGBoost outperformed rest of the models in predicting good song genres for each mental issue type and gave us good recommendations.






