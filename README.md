# Titanic-prediction-model
This project is a machine learning model built to predict the survival of passengers on the Titanic. The dataset used for this project is from Kaggle's Titanic:Machine Learning from Disaster competition (https://www.kaggle.com/competitions/titanic/data). The objective is to predict whether a passenger survived or not, based on features such as age, gender, class, and other attributes.

# Project Workflow
# 1. Data Preprocessing
- Cleaned the dataset by filling missing values, particularly in the Age, Cabin, and Embarked columns.
- Engineered new features, such as extracting the deck information from the Cabin feature.
- Converted categorical variables like Sex and Embarked into numerical formats for model training.

# 2. Feature Engineering
- Created a Deck feature from the Cabin column to capture additional insights.
- Mapped Sex, Embarked, to numerical values for use in the model and the Deck column was one-hot encoded to handle categorical information.

# 3. Model Training
- A Logistic Regression model was trained on the dataset to predict passenger survival.
- The model's performance was evaluated using precision, recall, F1-score, and accuracy metrics, along with a confusion matrix to visualize true positives, true negatives, false positives, and false negatives.

# 4. Evaluation Metrics
- Precision: 0.86
- Recall: 0.62
- F1-Score: 0.72
- Accuracy: 79%
  
# 5. Confusion Matrix Insights
The confusion matrix shows the true positive, true negative, false positive, and false negative predictions. From the matrix:
92 passengers who did not survive were correctly predicted.
49 passengers who survived were correctly predicted.
The model struggled with predicting survivors, with 30 false negatives (survived but predicted as not survived).

# Key Insights
- Deck B has the highest survival rate (0.63), and Deck C has the lowest survival rate (0.34).
- The model is more precise at predicting non-survivors than survivors, which could indicate a need for further tuning, particularly to improve recall for survivors.
- Survival by Ticket Class: Most passengers with a ticket class of 1 survived, while the majority in ticket class 3 did not.
- Survival rates show that more women survived than men, with men making up most of the non-survivors.
            - Male Passengers: 577 males.
            - Female Passengers: 314 females.
- There were 549 passengers who did not survive, while 342 passengers survived.

# Visualizations
The following visualizations were created to explore the dataset and gain insights:

- A countplot showing the number of survivors and non-survivors.
- A countplot visualizing the gender distribution of passengers (Male vs. Female).
- A countplot showing the survival rate by gender.
- A countplot showing the number of passengers per ticket class.
- A countplot visualizing survival rates by ticket class.
- A bar plot showing how survival rates differ based on passenger deck.
- Confusion matrix: A visual representation of the model's prediction accuracy.
These visualizations helped identify trends such as the impact of class and gender on survival rates.


# Conclusion
This project provided valuable insights into the factors that influenced survival on the Titanic. The logistic regression model performed reasonably well, with more accurate predictions for non-survivors compared to survivors. Future improvements could include testing other models like Random Forest or Gradient Boosting to potentially improve recall for survivors.

