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

<details>
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
          </ul>
        </li>
      </ul>
    </li>
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

## Project Structure
* `Bin` - Directory which stores all codes
  * `Project.Rmd` - The R markdown file for the project

* `Config` - Directory which stores all the configuration files
  * `kaggle.json` - A json file storing your Kaggle username and api key. (Replace this file with your own data)
  * `twitter.json` - A json file storing your Twitter API key, value, and bearer token. (Replace this file with your own data)

* `Data` - Directory which stores all data used in this project (will be auto-generated by R if not existed)
  * `Kaggle` - Directory which stores the dataset downloaded from Kaggle (wiil be auto-generated by R if not existed and the dataset will be downloaded to this file automatically)
  * `Twitter API Data` - Directory which stores the dataset we downloaded using Twitter API

* `Lexicon` - Directory which stores the lexicons we use for sentimental analysis
  * `NRC-Hashtag-Emotion-Lexicon-v0.2` - Directory for NRC Hashtag lexicon

* `Output` - Directory which stores all the output files
  * `Images` - Output Directory for images
  * `Rmd Knit` - Output Directory for Rmd Knit

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

## Contact

Feiyu Zheng - [feiyuzheng98@gmail.com](mailto:feiyuzheng98@gmail.com)

Junyi Li - [jl2707@scarletmail.rutgers.edu](mailto:jl2707@scarletmail.rutgers.edu)

Ziyu Zhou - [zz544@scarletmail.rutgers.edu](mailto:zz544@scarletmail.rutgers.edu)

Project Link: [https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets](https://github.com/ChaserZ98/Natural-Language-Processing-with-Disaster-Tweets)

<p align="right">(<a href="#top">back to top</a>)</p>