# IMDb Movie Review Sentiment Analysis

## Project Overview

This project applies Natural Language Processing (NLP) and machine learning to classify IMDb movie reviews as **positive or negative**.

The project uses text preprocessing and the Bag of Words (BoW) technique to convert reviews into numerical features. Three machine learning classifiers are trained and evaluated to compare their performance on sentiment classification.

## Dataset

The project uses the [IMDb Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) from Kaggle.

The dataset contains 50,000 movie reviews labeled as positive or negative.

| Column | Description |
|---|---|
| `review` | The text of the movie review |
| `sentiment` | The sentiment label: positive or negative |

The dataset is intended for binary sentiment classification and text analysis.

## Technologies Used

- Python
- Pandas
- NumPy
- NLTK
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## Project Workflow

### 1. Text Preprocessing

The review text is cleaned and prepared for machine learning. The preprocessing steps include:

- Removing non-alphabetic characters.
- Converting text to lowercase.
- Splitting reviews into individual words.
- Removing stopwords.
- Applying stemming to reduce words to their root forms.

### 2. Feature Extraction — Bag of Words

The Bag of Words technique is used to convert text reviews into numerical feature vectors based on word frequencies.

The vocabulary is limited to **5,000 features** in the current experiment.

### 3. Model Training

Three classification algorithms are evaluated:

- **Logistic Regression**
- **Linear Support Vector Machine (Linear SVM)**
- **Multinomial Naive Bayes**

### 4. Model Evaluation

The models are compared using test accuracy. A confusion matrix is also used to examine the correct and incorrect predictions made by the Logistic Regression model.

## Results

The following test accuracies were obtained using the current Bag of Words configuration.

| Classifier | Test Accuracy |
|---|---:|
| Logistic Regression | 87.13% |
| Linear SVM | 86.16% |
| Multinomial Naive Bayes | 73.45% |

**Best-performing model: Logistic Regression**, with a test accuracy of 87.13%.

### Confusion Matrix — Logistic Regression

The confusion matrix below summarizes the model's predictions on 10,000 test reviews.

|  | Predicted Negative | Predicted Positive |
|---|---:|---:|
| Actual Negative | 4,363 | 672 |
| Actual Positive | 615 | 4,350 |

Assuming negative is the first class and positive is the second:

- **True Negatives:** 4,363
- **False Positives:** 672
- **False Negatives:** 615
- **True Positives:** 4,350

The model correctly classified 8,713 out of 10,000 reviews, achieving 87.13% accuracy. It made slightly more false-positive predictions than false-negative predictions.

### Results Analysis

Logistic Regression achieved the highest accuracy among the three evaluated classifiers, outperforming Linear SVM by 0.97 percentage points. Multinomial Naive Bayes achieved a lower accuracy of 73.45% under the current configuration.

These results suggest that Logistic Regression was the most effective classifier in this experiment. However, performance may improve with further feature engineering and hyperparameter tuning.

## Conclusion

This project demonstrates a traditional machine learning approach to sentiment analysis, covering text preprocessing, feature extraction, model training, and evaluation.

Among the three evaluated classifiers, Logistic Regression achieved the best test accuracy at 87.13% using 5,000 Bag of Words features.

The experiment provides a baseline for further improvements in movie review sentiment classification.

## Future Improvements

- Experiment with larger vocabulary sizes.
- Incorporate bigram features to capture short phrases.
- Compare Bag of Words with TF-IDF.
- Perform hyperparameter tuning.
- Evaluate precision, recall, and F1-score for each classifier.
- Compare additional traditional machine learning and deep learning approaches.

## How to Run

1. Clone or download this repository.
2. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).
3. Install the required Python libraries.
4. Open the Jupyter Notebook in Jupyter Notebook or Google Colab.
5. Update the dataset path if necessary.
6. Run the notebook cells in order to reproduce the preprocessing, model training, and evaluation steps.

## Project Focus

Natural Language Processing (NLP) · Sentiment Analysis · Text Classification · Machine Learning
