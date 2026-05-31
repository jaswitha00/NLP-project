Objective
The objective of this assignment is to develop an NLP-based text classification model that automatically categorizes product reviews into Positive, Negative, or Neutral sentiment tags.

Dataset
The dataset dataset.csv contains 305 records representing diverse customer reviews:

sentiment: Target class labels ("positive", "negative", or "neutral").
review: Raw text comment submitted by the customer.
Technologies Used
Language: Python 3
Libraries:
pandas (Dataset management)
numpy (Algebraic evaluations)
scikit-learn (Splitting, TF-IDF vectorization, Logistic Regression classifier, and metrics)
re (Text token preprocessing)
Workflow
Text Preprocessing: Lowercases customer feedback, deletes symbols/numbers, and splits strings into individual tokens.
Stopwords Filtering: Employs a local standard list of English stopwords to clean text offline without requiring external NLTK downloads.
Feature Engineering: Vectorizes terms into numerical matrices using the standard Term Frequency-Inverse Document Frequency (TfidfVectorizer) algorithm.
Model Training: Performs a train-test split (80/20 ratio) and fits a multi-class softmax Logistic Regression model (LogisticRegression).
Model Evaluation: Generates metrics reports detailing accuracy, precision, recall, and a visual confusion matrix printed on screen.
Inference Playground: Evaluates three distinct custom text strings to demonstrate predictions and output probabilities.
How to Run
Navigate to the project directory:
cd NLP/Sentiment_Analysis
Install the requirements:
pip install -r requirements.txt
Run the python script:
python main.py
Expected Output
==================================================
       PROJECT 2: NLP - SENTIMENT ANALYSIS        
==================================================
Loading dataset: dataset.csv...
Dataset Loaded Successfully! Size: 305 records.
...
Accuracy Score: ~98.36%
...
Confusion Matrix:
               Predicted Neg  Predicted Neu  Predicted Pos
Actual Neg        20             0              0    
Actual Neu        0              19             0    
Actual Pos        1              0              21   
...
Testing Custom Reviews Inference:

Review: "This software is absolutely brilliant! Exceeded my expectations."
Predicted Sentiment: POSITIVE (Confidence: 81.35%)

Review: "It was highly overpriced for such cheap and bad quality."
Predicted Sentiment: NEGATIVE (Confidence: 89.24%)
