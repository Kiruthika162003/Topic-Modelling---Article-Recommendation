# Article Recommendation and Topic Modeling Project

## Overview

This project involves performing topic modeling using Latent Dirichlet Allocation (LDA) and Non-Negative Matrix Factorization (NMF). Additionally, an article recommendation engine was built using Term Frequency-Inverse Document Frequency (TF-IDF) and cosine similarity to suggest the most relevant documents based on a given keyword.

## Dataset

The dataset used for this project is a collection of Medium articles, which can be downloaded from [Kaggle](https://www.kaggle.com/hsankesara/medium-articles). The dataset contains the following columns:
- **author**: The author of the article
- **claps**: The number of claps the article received
- **reading_time**: The estimated reading time for the article
- **link**: The URL of the article
- **title**: The title of the article
- **text**: The full text of the article

## Steps Performed

### 1. Data Loading and Exploration
- Loaded the dataset using pandas.
- Displayed the first few rows of the dataset to understand its structure.
- Calculated the length of the text and title for each article and visualized the distributions using seaborn.

### 2. Data Preprocessing
- Downloaded and extended the list of stop words using NLTK.
- Created a function to clean and preprocess the text by removing punctuation, numbers, and stop words, and by lemmatizing the words.
- Created a dictionary representation of the documents and filtered out rare and common words.

### 3. Topic Modeling using LDA
- Built an LDA model using Gensim to identify topics in the articles.
- Visualized the topics using pyLDAvis to interpret the results.
- Displayed the top words for each topic.

### 4. Topic Modeling using NMF
- Built an NMF model using scikit-learn to identify topics in the articles.
- Displayed the top words for each topic.

### 5. Article Recommendation Engine
- Built a document recommender system using TF-IDF and cosine similarity.
- Given a keyword, the system suggests the most relevant articles from the dataset.

## Results

### Topic Modeling using LDA
The LDA model identified 10 topics in the articles. Here are the top words for each topic:

| Topic #01 | Topic #02 | Topic #03 | Topic #04 | Topic #05 | Topic #06 | Topic #07 | Topic #08 | Topic #09 | Topic #10 |
|-----------|------------|------------|------------|------------|------------|------------|------------|------------|------------|
| neuron    | star       | cpu        | de         | cluster    | bot        | car        | table      | pixel      | cnn        |
| activation| review     | house      | member     | agent      | conversation| music     | reward     | woman      | sheet      |
| matrix    | rating     | gtx        | sound      | policy     | behavior   | graph      | startup    | men        | box        |
| zero      | average    | sentence   | title      | host       | social     | batch      | recognize  | convolution| region     |
| player    | weighted   | gpu        | speech     | response   | simulation | vehicle    | array      | kernel     | pixel      |

### Topic Modeling using NMF
The NMF model also identified 10 topics in the articles. Here are the top words for each topic:

| Topic #01 | Topic #02 | Topic #03 | Topic #04 | Topic #05 | Topic #06 | Topic #07 | Topic #08 | Topic #09 | Topic #10 |
|-----------|------------|------------|------------|------------|------------|------------|------------|------------|------------|
| you       | feature    | policy     | you        | bot        | you        | you        | you        | you        | you        |
| ml        | features   | learning   | functions  | the        | good       | good       | good       | good       | good       |
| learning  | featuretools| learn     | list       | bots       | happening  | happening  | happening  | happening  | happening  |
| machine   | data       | actions    | functions  | it         | hand       | hand       | hand       | hand       | hand       |
| course    | primitives | deep       | data       | chatbots   | guis       | guis       | guis       | guis       | guis       |

### Article Recommendation Engine
The recommendation engine suggests the most relevant articles based on a given keyword. For example, given the keyword "news", the top recommended articles are:
1. How Artificial Intelligence can improve online news
2. The 7 Best Data Science and Machine Learning Podcasts
3. The Rise of the Weaponized AI Propaganda Machine – Scout: Science Fiction + Journalism – Medium
4. AI is coming, and it will be boring – Denny Vrandečić – Medium
5. ИИ-психопат и ИИ-обманщик – Hey Machine Learning
