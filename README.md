# Marvel Character Backstory Sentiment Analysis

## Introduction
In this project, we aimed to predict the emotional sentiment—specifically the level of sadness—in the backstories of Marvel Characters using a logistic regression model. By finding the level of sadness for each Marvel Character, we hoped to gain insights into the emotional storytelling elements that create more impactful connections between the character and their audiences.

## Objectives
1. Build a dataset of Marvel Character backstories, along with a sadness score based on Python Sentiment Analysis.
2. Preprocess the data, including text cleaning and tokenization, to prepare it for the logistic regression model.
3. Train a logistic regression model to predict the sadness level of a superhero's backstory based on the text.
4. Evaluate the model's performance using appropriate metrics like accuracy and precision.

## Tech Stack & Libraries
* **Language:** Python 3
* **Data Manipulation:** `pandas`, `numpy`
* **Natural Language Processing (NLP):** `nltk` (VADER SentimentIntensityAnalyzer), `contractions`, `CountVectorizer`
* **Machine Learning:** `scikit-learn` (Logistic Regression, RandomForestRegressor)
* **Data Balancing:** `imbalanced-learn` (SMOTE)
* **Data Visualization:** `matplotlib`, `seaborn`

## Methodology
1. **Sentiment Extraction:** Utilized NLTK's VADER SentimentIntensityAnalyzer to extract a "negative" (`neg`) sentiment score from the cleaned text of each character's backstory. 
2. **Categorization:** Converted the continuous sadness scores into four distinct classification buckets: `a little sad`, `somewhat sad`, `moderately sad`, and `sad`.
3. **Handling Class Imbalance:** Addressed the heavy skew in the dataset (e.g., 354 characters classified as 'somewhat sad' vs. only 5 classified as 'sad') by utilizing **SMOTE** (Synthetic Minority Over-sampling Technique) to synthetically balance all classes to 354 samples each.
4. **Model Training:** Vectorized the text features using `CountVectorizer` and trained a Logistic Regression classifier on a 70/30 train-test split.

## Results and Conclusion
After collecting and preprocessing the data, we successfully trained a Logistic Regression model to predict the sadness level of Marvel Character backstories. The resulting model performed exceptionally well, achieving an **accuracy of ~86.8%** on the test dataset. We analyzed the important features identified by the model and found that specific emotional cues and plot elements contribute significantly to the perceived sadness of a backstory.

## Acknowledgments
We would like to express our gratitude to Jonathan Besomi for providing us with the data and the opportunity to work on this exciting project. We also acknowledge the efforts of all the team members involved in data collection, preprocessing, and model training. 

**Team Members:** * Ezana Enquobahrie
* Logan
* Ashley (Mentor)
