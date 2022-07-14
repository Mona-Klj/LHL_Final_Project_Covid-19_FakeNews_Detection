# LHL_Final_Project
This repo contains data and codes of my capstone project at <a href="https://www.lighthouselabs.ca/"> Lighthouse Labs</a> data science Bootcamp.

## Covid_19 Fake News Detection
The widespread problem of fake news is very difficult to tackle in today’s digital world where there are thousands of information-sharing platforms through which fake news or misinformation may propagate. It has become a greater issue because of the advancements in AI which brings along artificial bots that may be used to create and spread fake news. The situation is dire because many people believe anything they read on the internet and the ones who are amateur or are new to digital technology may be easily fooled.
Since its emergence in December 2019, there have been numerous posts and news regarding the COVID-19 pandemic on social media, traditional print, and electronic media. These sources have information from both trusted and non-trusted medical sources. Furthermore, the news from these media is spread rapidly. There have been instances where the situation has gone out of control because people acted without verifying the authenticity of the news.  
Therefore, a model for detecting fake news from the news pool is essential. In this work, the dataset which is a fusion of news related to COVID-19 that has been sourced from data from several social media and news sources is used for classification. 

## Data Preprocessing
The dataset which is used for this project is from https://www.sciencedirect.com/science/article/pii/S1568494621003161 that contain 22000 row of labelled tweet about covid-19 news.
In the first step, preprocessing is performed on the dataset by the NLP techniques to remove unwanted text (removing stopwords, text stemming, removing punctuations), then splitting has carried out to extract the tokens from the raw text data. Later, feature engineering as vectorizing the words has performed by using the Tfidf vectorizer. 

### Modelling and Evaluating
In this step, several state-of-the-art machine learning algorithms are trained to classify the COVID-19-related dataset. The Classifier algorithms (Lodistic Regression, Decision Tree, Randon Forst, Passive Aggressinve, Multinomial Naive Bayes, Gradient Boosting and SVM ) are then evaluated using various metrics in <a href="https://github.com/Mona-Klj/LHL_Final_Project/blob/main/covidnews_Modeling.ipynb"> covidnews_Modeling.ipynb </a>notebook. The results show that the Passive-Aggressive and SVM classifier outperforms the other classifiers with an accuracy of 98%. But I chose Passive_Agressive over SVM because of fewer false positives on Fake news and stability in all scores.
Next, the Passive-Aggressive classifier algorithm is used to detect fake news items. This algorithm is called so because it is passive in the case of correct classification and is aggressive if there is a miscalculation. 

## Deploying by Flask  
And in the last step, I deployed my model with a Flask web app. You can run <a href="https://github.com/Mona-Klj/LHL_Final_Project/blob/main/Fake_News_Det.py"> Fake_News_Det.py</a> in root directory with model.pkl to see the web app runnig.
