# Twitter Sentiment Analysis with Natural Language Processing

**Author**: [Christie Sarver](mailto:christie.sarver@gmail.com)

## Overview

The goal of this project is to build a model that can classify the sentiment of a tweet based on its contents. This is a multiclass problem, where sentiments are either negative, positive, or neutral. 

The data was manually labeled for classification, and contains the tweet text, the product or brand mentioned, and the sentiment as interpreted by the labeler.

### The Data

The data used is sourced from Twitter from SXSW 2013, and contains tweets about the SXSW tech events and product announcements. Most of the tweets are about Apple and Google products, so I will analyze sentiment for each brand. The raw data can be found in the data folder in this repository.

The data presented a challenge in terms of class imbalance; the majority of the data was labeled as 'neutral', leaving a relatively small amount of samples that indicated actual sentiment, positive or negative. 

### Business Problem

The resulting model will be used to classify tweets from future tech conferences from Google and Apple, and analyze how sentiment for the brands has changed over time.

## Methodology - update

A variety of pre-processing and modeling techniques were explored in order to effectively transform the text data and build a strong classifier. 

Preprocessing included:

* Location-based indicators: latitude, longitude, basin, distance to land
* Weather conditions: wind speed, storm speed, storm direction
* Times of occurence: year, week of year

Model types explored were:

These methods were evaluated based on their accuracy scores. They were examined to understand where error was occuring in order to optimize. 

## Results - update

Based on the model evaluations which are detailed in the notebook, the final model chosen to move forward with is a boosted method using Adaboost. The strenghts of this model include its high recall score as compared to others and overall high accuracy.

Areas where the model could be improved include reducing overall error as shown in the confusion matrix below.

![confusion_matrix.png](./images/confusion_matrix.png)

### Conclusions & Future Work - update

The Adaboost model can be further tuned to reduce error, and other boosting methods can be exploredto see how they compare. It is also recommended to revisit the feature selection to potentially remove more of the less trustworthy features to get better predictions.

This data set itself presented several challenges. For future work it is recommended to work closer with or take further time to examine/understand NOAA data and their methodology in order to improve data that is piped into this model. This may include examining the different sources of the data as well as the data gathering process.

Lastly, while this project analyzed individual readings in the data, it is recommended to analyze data grouped by storm if more instances of the 0 class are able to be added to the data set to take a more holistic look at storm patterns.

## For More Information - update

Please reference the [Jupyter Notebook](./Data%20Classification_Predicting%20Tropical%20Storms.ipynb) or review this [presentation](./Data%20Classification%20Presentation.pdf).

## Repository Structure - update

```
├── images
├── Data Classification_Predicting Tropical Storms.ipynb
├── Data Visualizations.ipynb
├── IBTrACS_version4_Technical_Details.pdf
├── Data Classification Presentation.pdf
├── README.md

```
Thank you!
