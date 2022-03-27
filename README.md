# Natural Language Processing with Disaster Tweets

### Predict which Tweets are about real disasters and which ones are not

Language: ![R](https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white)

Data Source: ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)

R Packages: ![tidyverse version](https://img.shields.io/badge/tidyverse-1.3.1-brightgreen)
![dplyr version](https://img.shields.io/badge/dplyr-1.0.7-brightgreen)
![ggplot2 version](https://img.shields.io/badge/ggplot2-3.3.5-brightgreen)


- [Competition Description](#competition-description)


## Competition Description
Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

But, it’s not always clear whether a person’s words are actually announcing a disaster. Take this example:

<img width = '300' height = '550' src = "https://storage.googleapis.com/kaggle-media/competitions/tweet_screenshot.png"/>

The author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine.

In this competition, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified. If this is your first time working on an NLP problem, we've created a quick tutorial to get you up and running.

Disclaimer: The dataset for this competition contains text that may be considered profane, vulgar, or offensive.
