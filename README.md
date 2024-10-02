# YouTube Video Sentiment Analysis and Regression

## Overview
This project involves sentiment analysis of YouTube video comments by extracting data from the most liked, disliked, and random videos. Using machine learning models such as Random Forest, Ridge, and Gradient Boosting, it aims to predict video performance metrics and views based on sentiment analysis scores. The project also includes hyperparameter tuning and model stacking for improved predictive accuracy.

## Table of Contents
- [Data Collection](#data-collection)
- [Sentiment Analysis](#sentiment-analysis)
- [Machine Learning Models](#machine-learning-models)
- [Model Tuning and Stacking](#model-tuning-and-stacking)
- [Conclusion](#conclusion)

## Data Collection
The dataset is collected from YouTube using the Google API. Comments are extracted for three categories:
1. **Most Liked Videos**: Top 8,000 videos with the highest number of likes.
2. **Most Disliked Videos**: Top 8,000 videos with the highest number of dislikes.
3. **Random Videos**: 8,000 randomly selected videos from the dataset.

## Sentiment Analysis
We use the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool to analyze the extracted comments. The sentiment scores are then used to help predict video performance in the machine learning phase.

## Machine Learning Models
Several regression models are applied to predict video metrics (likes/dislikes):
1. **Random Forest Regression**
2. **Ridge Regression**
3. **K-Nearest Neighbors Regression**
4. **Gradient Boosting Regression**

These models are trained and tested on the dataset, with metrics such as R² scores used to evaluate their performance.

## Model Tuning and Stacking
To improve model performance, hyperparameter tuning is done for both Random Forest and Gradient Boosting models. Stacking is also implemented to combine the strengths of multiple models for better results.

## Conclusion and Future Work
Stacking, an advanced ensemble technique, excels in generalization as
demonstrated by its robust performance on the testing set. By leveraging the
complementary strengths of multiple base regression models, stacking aggregates
their predictions to achieve superior accuracy compared to any single model. This
not only mitigates the limitations of individual models but also optimizes
predictive performance, making it highly suitable for applications prioritizing
precision.
In future, there are promising avenues for further improvement and exploration.
One key focus could be on reducing the Mean Squared Error (MSE) by refining
feature selection techniques or introducing novel features that capture additional
relevant information. Furthermore, enhancing the interpretability of the stacked
model would provide valuable insights into how different base models contribute
to predictions, thereby fostering trust and facilitating informed decision-making in
real-world scenarios. Overall, continuous refinement and innovation in stacking
methodology hold significant potential to deliver more precise and actionable
predictions in diverse applications.

## Usage
To run this notebook, you will need the following libraries installed:
- pandas
- vaderSentiment
- matplotlib
- google-api-python-client
- scikit-learn

You can install them using pip:
```bash
pip install pandas vaderSentiment matplotlib google-api-python-client scikit-learn
