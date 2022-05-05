<div id="top"></div>

[![commits](https://badgen.net/github/commits/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/main)](https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/graphs/commit-activity)
[![forks](https://badgen.net/github/forks/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets)](https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/network/members)
[![stars](https://badgen.net/github/stars/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets)](https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/stargazers)
[![issues](https://badgen.net/github/issues/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets)](https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/issues/)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)

<div align="center">
  <h1 align="center">Natural Language Processing with Disaster Tweets</h1>
  <p align="center">
    Predict which Tweets are about real disasters and which ones are not
    <br />
    <a href="https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets">View Demo</a>
    ·
    <a href="https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/issues">Report Bug</a>
    ·
    <a href="https://GitHub.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/issues">Request Feature</a>
  </p>
</div>

<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
        <li><a href="#purpose">Purpose</a></li>
      </ul>
    </li>
    <li><a href="#project-structure">Project Structure</a></li>
    <li>
      <a href="#project-overview">Project Overview</a>
      <ul>
        <li>
          <a href="#dataset-overview">Dataset Overview</a>
          <ul>
            <li><a href="#columns">Columns</a></li>
            <li><a href="#missing-value">Missing Value</a></li>
            <li><a href="#target-distribution">Target Distribution</a></li>
            <li><a href="#word-cloud-for-text">Word Cloud for text</a></li>
            <li><a href="#usa-disaster-distribution">USA Disaster Distribution</a></li>
          </ul>
        </li>
        <li><a href="#data-cleaning">Data Cleaning</a></li>
        <li><a href="#latent-dirichlet-allocation-lda">Latent Dirichlet Allocation (LDA)</a></li>
        <li>
          <a href="#Feature Engineering">Feature Engineering</a>
          <ul>
            <li><a href="#numeric">Numeric</a></li>
            <li><a href="#ratio-analysis">Ratio Analysis</a></li>
            <li><a href="#sentiment-analysis">Sentiment Analysis</a></li>
          </ul>
        </li>
        <li>
          <a href="#classifier-model-training">Classifier Model Training</a>
          <ul>
            <li><a href="#train-validation-split">Train-validation Split</a></li>
            <li><a href="#random-forest">Random Forest</a></li>
            <li><a href="#neural-network">Neural Network</a></li>
          </ul>
        </li>
        <li><a href="#performance-on-test-set-using-random-forest-bagging">Performance on Test Set Using Random Forest (Bagging)</a></li>
      </ul>
    </li>
    <li><a href="#reference">Reference</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

## About The Project

This is a course project of Rutgers MSDS597 Data Wrangling and Husbandry.

### Built with

* Language:
  ![R](https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white)

* Data Source: ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)
  
  [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started)

* R Packages:
  ![tidyverse version](https://img.shields.io/badge/tidyverse-1.3.1-brightgreen)
  ![dplyr version](https://img.shields.io/badge/dplyr-1.0.7-brightgreen)
  ![ggplot2 version](https://img.shields.io/badge/ggplot2-3.3.5-brightgreen)
  ![tidytext version](https://img.shields.io/badge/tidytext-0.3.2-brightgreen)
  ![textdata version](https://img.shields.io/badge/textdata-0.4.1-brightgreen)
  ![rvest version](https://img.shields.io/badge/rvest-1.0.2-brightgreen)
  ![httr version](https://img.shields.io/badge/httr-1.4.2-brightgreen)
  ![curl version](https://img.shields.io/badge/curl-4.3.2-brightgreen)
  ![jsonlite version](https://img.shields.io/badge/jsonlite-1.7.3-brightgreen)
  ![caret version](https://img.shields.io/badge/caret-6.0--91-brightgreen)
  ![gridExtra version](https://img.shields.io/badge/gridExtra-2.3-brightgreen)
  ![scales version](https://img.shields.io/badge/scales-1.1.1-brightgreen)
  ![choroplethr version](https://img.shields.io/badge/choroplethr-3.7.0-brightgreen)
  ![choroplethrMaps version](https://img.shields.io/badge/choroplethrMaps-1.0.1-brightgreen)
  ![topicmodels version](https://img.shields.io/badge/topicmodels-0.2--12-brightgreen)
  ![textmineR version](https://img.shields.io/badge/textmineR-3.0.5-brightgreen)
  ![wordcloud2 version](https://img.shields.io/badge/wordcloud2-0.2.2-brightgreen)
  ![gbm version](https://img.shields.io/badge/gbm-2.1.8-brightgreen)
  ![randomForest version](https://img.shields.io/badge/randomForest-4.7--1-brightgreen)
  ![neuralnet version](https://img.shields.io/badge/neuralnet-1.44.2-brightgreen)

### Purpose
The project is based on Natural Language Processing with Disaster Tweets competition on Kaggle. We are trying to build a classifier to distinguish whether a public tweet is aboud disaster or not.

#### Competition Description
Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

But, it’s not always clear whether a person’s words are actually announcing a disaster. Take this example:

<img width = '200' height = '400' src = "https://storage.googleapis.com/kaggle-media/competitions/tweet_screenshot.png"/>

The author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine.

In this competition, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified. If this is your first time working on an NLP problem, we've created a quick tutorial to get you up and running.

Disclaimer: The dataset for this competition contains text that may be considered profane, vulgar, or offensive.

<p align="right">(<a href="#top">back to top</a>)</p>

## Project Structure
* `Bin` - Directory which stores all codes
  * `Project.Rmd` - The R markdown file for the project

* `Config` - Directory which stores all the configuration files
  * `kaggle.json` - A json file storing your Kaggle username and api key. (Replace this file with your own data)
  * `twitter.json` - A json file storing your Twitter API key, value, and bearer token. (Replace this file with your own data)

* `Data` - Directory which stores all data used in this project (will be auto-generated by R if not existed)
  * `Kaggle` - Directory which stores the dataset downloaded from Kaggle (the directory wiil be auto-generated by R if not existed and the dataset will be downloaded to this directory automatically)
  * `Twitter API Data` - Directory which stores the dataset we downloaded using Twitter API

* `Lexicon` - Directory which stores the lexicons we use for sentimental analysis
  * `NRC-Hashtag-Emotion-Lexicon-v0.2.txt` - NRC Hashtag Lexicon

* `Output` - Directory which stores all the output files
  * `Images` - Output Directory for images
  * `Rmd Knit` - Output Directory for Rmarkdown Knit
  * `Presentation Slides` - Directory for presentation slides

<p align="right">(<a href="#top">back to top</a>)</p>

## Project Overview

### Dataset overview

#### Columns
  * `id` - unique identifier for each tweet
  * `keyword` - keyword of the text content
  * `location` - location of the tweet
  * `text` - text content of each tweet
  * `target` - binary value (0 for non-disaster tweet and 1 for disaster tweet)

#### Missing Value
  <img width = '450' height = '350' alt="missing value plot" title="missing value plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/missing%20value%20plot.png?raw=true"/>

#### Target distribution
  <img width = '450' height = '300' alt="target distribution plot" title="target distribution plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/target%20distribution%20plot.png?raw=true"/>

#### Word Cloud for `text`
  * Word cloud for all tweets
    
    <img width = '450' height = '300' alt="word cloud all" title="word cloud all" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/wordcloud%20all.png?raw=true"/>

  * Word cloud for disaster tweets

    <img width = '450' height = '300' alt="word cloud all" title="word cloud all" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/wordcloud%20disaster.png?raw=true"/>

#### USA Disaster Distribution

  <img width = '450' height = '300' alt="usa disaster map" title="usa disaster map" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/disaster%20map.png?raw=true"/>

### Data Cleaning
  * Clean mislabeled tweets
  * Extract links from `text` - get `link_count`
  * Convert special url character (%20 as white space) to readable string and replace newline character \n in text - get `line_count`
  * Extract tags and '@'s from `text` - get `tag_count` and `at_count`

### Latent Dirichlet Allocation (LDA)
  * Tokenization
  * Create Document Term Matrix (DTM)
  * Model Tuning

    <img width = '450' height = '300' alt="coherence plot" title="coherence plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/coherence%20plot.png?raw=true"/>
  * Topics
  
    <img width = '450' height = '300' alt="topic plot" title="topic plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/topic%20plot.png?raw=true"/>

### Feature Engineering

#### Numeric
  * `link_count` - number of links in a tweet
  * `line_count` - number of lines in a tweet
  * `tag_count` - number of tags in a tweet
  * `at_count` - number of '@'s in a tweet
  * `char_length` - number of characters in a tweet
  * `word_count` - number of words in a tweet
  * `mean_word_length` - derived by <img src="https://latex.codecogs.com/png.latex?%5Cbg_white\frac{\text{char\_length}}{\text{word\_count}}" title="\frac{\text{char\_length}}{\text{word\_count}}"/>, the average number of characters used for a word in a tweet

  * `unique_word_count` - the number of distinct words used in a tweet
  * `punc_count` - the number of punctuation marks in a tweet
  * `stop_word_count` - the number of stop words in a tweet
    <img width = '450' height = '300' alt="distribution plot" title="distribution plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/distribution%20plot.png?raw=true"/>

#### Ratio Analysis
  * Extract common disaster and non-disaster keyword, tags, '@'s and n-grams
  * N-gram analysis
    * Unigram

      <img width = '450' height = '300' alt="top 20 unigram plot" title="top 20 unigram plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/top20Unigram%20plot.png?raw=true"/>
    * Bigram
      
      <img width = '450' height = '300' alt="top 20 bigram plot" title="top 20 bigram plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/top20Bigram%20plot.png?raw=true"/>
    * Trigram
      
      <img width = '450' height = '300' alt="top 20 trigram plot" title="top 20 trigram plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/top20Trigram%20plot.png?raw=true"/>

#### Sentiment Analysis
  * Lexicon: [NRC-Hashtag-Emotion-Lexicon-v0.2](https://saifmohammad.com/WebPages/NRC-Emotion-Lexicon.htm) <sup>[<a href="#reference-1">1</a>, <a href="#reference-2">2</a>]</sup>
    * score: real-valued score between 0 to <img src="https://latex.codecogs.com/png.latex?%5Cbg_white\infty" title="\infty" />
    * size: 16862 unigrams
    * emotions
      * positive: anticipation, joy, surprise, trust
      * negative: anger, disgust, fear, sadness
  * `Sentimental Score` - sum of 4 positive sentiments scores minus sum of 4 negative sentiments scores

### Classifier Model Training

#### Train-validation Split
  * 80% train - 43% disaster tweet, 57% non-disaster tweet
  * 20% validatoin - 43% disaster tweet, 57% non-disaster tweet

#### Random Forest
  * Bagging
    * package: randomForest
    * ntree: 2000
    * accuracy on validation set: 77.78%
    * confusion matrix on validation set:

      <img src="https://latex.codecogs.com/png.latex?%5Cbg_white\begin{matrix}&\text{Reference}&\\\text{Prediction}&0&1\\0&752&223\\1&115&431\end{matrix}" title="bagging confusion matrix" />

  * Boosting
    * package: gbm
    * ntree: 5000
    * ineraction depth: 3
    * shrinkage: 0.2
    * accuracy on validation set: 76%
    * confusion matrix on validation set:
      
      <img src="https://latex.codecogs.com/png.latex?%5Cbg_white\begin{matrix}&\text{Reference}&\\\text{Prediction}&0&1\\0&735&233\\1&132&421\end{matrix}" title="boosting confusion matrix" />

#### Neural Network
  * package: neuralnet
  * number of hidden node: 5
  * min threshold: 0.06
  * activation function: logistic
  * error function: ce
  * stepmax: 1000000
  * accuracy on validation set: 75.61%
  * confusion matrix on validation set:
  
    <img src="https://latex.codecogs.com/png.latex?%5Cbg_white\begin{matrix}&\text{Reference}&\\\text{Prediction}&0&1\\0&716&151\\1&220&434\end{matrix}" title="neural network confusion matrix" />

  * visualization:
    
    <img width = '450' height = '300' alt="top 20 unigram plot" title="top 20 unigram plot" src = "https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Output/Images/neural%20network%20plot.png?raw=true"/>

### Performance on Test Set Using Random Forest (Bagging)
  * accuracy: 75.45%
  * confusion matrix on validation set:

    <img src="https://latex.codecogs.com/png.latex?%5Cbg_white\begin{matrix}&\text{Reference}&\\\text{Prediction}&0&1\\0&1566&504\\1&297&896\end{matrix}" title="test confusion matrix" />

<p align="right">(<a href="#top">back to top</a>)</p>

## Reference

<p id="reference-1"></p>

[1] [*Using Hashtags to Capture Fine Emotion Categories from Tweets*](http://saifmohammad.com/WebDocs/hashtags-MK.pdf). Saif M. Mohammad, Svetlana Kiritchenko, Computational Intelligence, Volume 31, Issue 2, Pages 301-326, May 2015.

<p id="reference-2"></p>

[2] [*#Emotional Tweets*](http://ixa2.si.ehu.es/starsem/proc/pdf/STARSEM-SEMEVAL033.pdf), Saif Mohammad, In Proceedings of the First Joint Conference on Lexical and Computational Semantics (*Sem), June 2012, Montreal, Canada.
<p align="right">(<a href="#top">back to top</a>)</p>

## Contact

Feiyu Zheng - [feiyuzheng98@gmail.com](mailto:feiyuzheng98@gmail.com)

Junyi Li - [jl2707@scarletmail.rutgers.edu](mailto:jl2707@scarletmail.rutgers.edu)

Ziyu Zhou - [zz544@scarletmail.rutgers.edu](mailto:zz544@scarletmail.rutgers.edu)

Project Link: [https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets](https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets)

<p align="right">(<a href="#top">back to top</a>)</p>