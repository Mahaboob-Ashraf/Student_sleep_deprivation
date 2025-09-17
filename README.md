# Student Sleep Deprivation Prediction

##  Project Overview

This project explores the factors contributing to sleep deprivation in students by building a predictive machine learning model. Using **Logistic Regression**, the model analyzes a student's daily habits—such as study hours, screen time, and caffeine intake—to classify whether they are sleep-deprived. The goal is to create a reliable classifier that can help identify patterns related to sleep health among students.

---

##  Dataset and Features

The model is trained on the `student_sleep_deprivation_dataset.csv`, which contains 500 entries. The key features used for prediction include:

* **Lifestyle Habits**: `sleep_hours`, `study_hours`, `screen_time_hours`
* **Physical Activity**: `physical_activity_mins`
* **Consumption**: `caffeine_cups`
* **Well-being**: `mood_score` (categorical: Low, Medium, High)
* **Schedule**: `wake_up_time_hour`

---

##  Methodology

The core of the project is a Python script utilizing powerful data science libraries.

1.  **Data Preprocessing**: The script begins by loading the dataset with **`pandas`**. A crucial preprocessing step involves converting the categorical `mood_score` column into a numerical format using `scikit-learn`'s `LabelEncoder`, making it compatible with the machine learning algorithm.

2.  **Model Training**: The dataset is split into an 80% training set and a 20% testing set. A **`LogisticRegression`** model from **`scikit-learn`** is then trained on the training data to learn the relationship between the input features and the likelihood of sleep deprivation.

3.  **Evaluation**: After training, the model's predictive power is tested on the unseen data. The evaluation focuses on how accurately the model can classify students.

---

##  Results and Evaluation

The trained model demonstrates strong predictive performance, achieving an overall **accuracy of 85%** on the test set.

To provide a more detailed assessment, a **Classification Report** is generated, offering insights into the precision, recall, and F1-score for both the 'Deprived' and 'Not Deprived' classes. A **Confusion Matrix**, visualized with `seaborn` and `matplotlib`, is also created to clearly show the model's correct and incorrect predictions.
