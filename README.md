# Twitter Sentiment Analysis with Natural Language Processing

**Author**: [Christie Sarver](mailto:christie.sarver@gmail.com)

## Overview

The goal of this project is to build a model that can classify the sentiment of a tweet based on its contents. This is a multiclass problem, where sentiments are either negative, positive, or neutral. 

The data was manually labeled for classification, and contains the tweet text, the product or brand mentioned, and the sentiment as interpreted by the labeler.

### The Data

The data used is sourced from Twitter from SXSW 2013, and contains tweets about the SXSW tech events and product announcements. Most of the tweets are about Apple and Google products, so I will analyze sentiment for each brand. The raw data can be found in the data folder in this repository.

The data presented a challenge in terms of class imbalance; the majority of the data was labeled as 'neutral', leaving a relatively small amount of samples that indicated actual sentiment, positive or negative. 

![sentiment_bars.png](./Images/sentiment_bars.png)

### Business Problem

The resulting model will be used to classify tweets from future tech conferences from Google and Apple, and analyze how sentiment for the brands has changed over time.

## Methodology 

A variety of pre-processing and modeling techniques were explored in order to effectively transform the text data and build a strong classifier. Model performance was evaluated on accuracy scores to suit the business goal of building an accurate model for future use.  

Preprocessing included:

* Data cleaning and exploration to sort into relevant categories
* Tokenization of words and removal of stop words and grammar. Twitter handles and URLs were also removed
* Vectorization of text data using diffent strategies such as Count Vectorization and TF-IDF

Model types explored were:

* Bayesian Classifiers
* Support Vector Machines
* Neural Nets

## Results

Out of all the iterations of models that I tried, the neural nets using GloVe were most sucessful in achieving high accuracy. However, after trying several different techniques, the overfitting problem still didn't improve too much. The final model iteration used L1 regularization and included drop out layers to reduce sensitivity to variance. 

My final neural net achieved 98% accuracy on the training set but 64% on the test set. I would recommend moving forward with this model to evaluate sentiment around future events and conferences related to tech as it has learned off of a specified data set.

![neural_net_accuracy.png](./Images/neural_net_accuracy.png)

### Conclusions & Future Work

This data set presented the challenge of a pretty extreme class imbalance. Since the majority of samples were labeled as neutral, there were fewer indicators of sentiment.

The classifiers typically used for text data don't have as many hyper-parameters that can be tuned to correct for class imbalance. Compliment Naive Bayes was applied to help with this, and and SVM model was used in hopes of reducing overfitting. However the most satisfactory results came from the neural net.

In order to improve this model and make in more generalizable, it is recommended to gather more data that has a higher percentage of labels that indicate positive or negative sentiment. Adding more data could also allow the use of a simpler neural net model, which could help to reduce runtimes.

## For More Information

Please reference the [Jupyter Notebook](./Final%20Notebook.ipynb) or review this [presentation](./Sentiment%20Analysis%20with%20Twitter%20NLP.pdf).

## Repository Structure

```
├── Archive
├── Images
├── Data
├── Final Notebook.ipynb
├── Sentiment Analysis with Twitter NLP.pdf
├── README.md

```
Thank you!
