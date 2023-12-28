# SMS Spam Detection: NLP

## 1. Data Cleaning

* Objective: Prepare the dataset for analysis and model training by addressing missing values, duplicates, and irrelevant columns.

* Data Loading and Inspection:
  - Loaded the 'spam.csv' dataset with encoding "ISO-8859-1".
  - Explored the structure of the dataset with a focus on the initial entries and random samples.
  - Checked the shape of the dataset, revealing 5572 entries and 5 columns.

* Handling Missing Values:
  - Investigated missing values in the dataset using `df.info()`.
  - Dropped three columns ('Unnamed: 2', 'Unnamed: 3', 'Unnamed: 4') with high null values.
  - Renamed the remaining columns to 'target' and 'sms_text'.

* Label Encoding:
  - Encoded the 'target' column ('ham' or 'spam') numerically using scikit-learn's LabelEncoder.

* Handling Duplicates:
  - Explored and identified 403 duplicate entries.
  - Removed duplicates, resulting in a dataset with 5169 entries.

## 2. Exploratory Data Analysis (EDA)

* Objective: Understand the distribution and characteristics of the dataset.

* Statistical Analysis:
  - Utilized descriptive statistics to analyze numerical features such as the number of characters, words, and sentences in the messages.
  - Conducted separate analyses for ham and spam messages, revealing variations in character count, word count, and sentence count.

* Data Visualization:
  - Created pie charts to visualize the class distribution, highlighting the imbalance between ham and spam messages.
  - Employed histograms and pair plots for numerical features, providing insights into the underlying patterns.
  
## 3. Text (Data) Preprocessing

* Objective: Prepare the text data for model training by applying various preprocessing techniques.

* Text Transformation:
  - Lowercased the text data.
  - Tokenized and removed special characters.
  - Removed stop words and punctuation.
  - Applied stemming using the Porter Stemmer from NLTK.

* Word Cloud Visualization:
  - Utilized WordCloud to visualize the most frequent words in both spam and ham messages.

## 4. Model Building

* Objective: Develop machine learning models for SMS spam detection.

* Feature Extraction:
  - Used CountVectorizer to convert text data into numerical format suitable for model training.
  - Obtained a feature matrix with 6708 features.

* Model Selection:
  - Implemented three Naive Bayes models – Gaussian, Multinomial, and Bernoulli.
  
* Model Evaluation:
  - Evaluated models based on accuracy, precision, and confusion matrices.
  - Gaussian Naive Bayes achieved an accuracy of 88.01% and precision of 53.15%.
  - Multinomial Naive Bayes outperformed with an accuracy of 96.42% and precision of 83.44%.
  - Bernoulli Naive Bayes demonstrated exceptional accuracy (97.00%) and precision (97.35%), making it the preferred model for spam detection.

## Conclusion

The SMS spam detection project successfully addressed data cleaning, exploratory data analysis, text preprocessing, and model building. Leveraging Naive Bayes models, particularly the Bernoulli Naive Bayes, the project demonstrated high accuracy and precision in distinguishing between spam and ham messages. The comprehensive approach to data preprocessing and thoughtful model selection showcased the effectiveness of the developed system in combating unwanted SMS communication.
