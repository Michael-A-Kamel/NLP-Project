# Twitter NLP Topic Modeling Analysis for Crypto Hedge Fund
Michael Kamel

## Abstract
Whenever it comes to hedge funds, there is a high premium placed on valuable and unique investing information. Crypto hedge funds are no different. However, they are not currently struggling. According to PWC, crypto hedge funds had a median return of 128% in 2020, up from 30% in 2019. Additionally, discretionary long only strategies generated 294% returns, while quantitative strategies generated 72% returns. My project is targetted at the discretionary long strategies. Specifically, the goal of my project is to empower these hedge fund's research teams by providing them with analysis of retail investor opinion, through Twitter NLP Topic Modeling. Via NMF models, I was able to distinguish some meaningful groupings of tweets for research analysis, with some indication of corrleation between price and topic prevelance.

## Design

## Data
I utilized Snscrape, a Python Scraping Library geared toward social networking services (SNS), to scrape 500K tweets with #Solana. From there, I filtered the data to only include tweets with 3 or more likes, and pre-processed the tweets to be ready for tokenization (lower-case, no puncutation, turning emojis to text). Then, I tokenized the cleaned tweets using NLTK, finalization preparation for modeling.

## Algorithms
TD-IDF was most suited for vectorization for this problem, as there is plenty of repetition amongst crypto tweets (naming of the various crypto assets, for instance). In terms of topic modeling, NMF was most suitable, as the documents were short, and there is naturally an emphasis on interpretability, given the use case (research). Both of these factors play into the strenghts of NMF modeling. In terms of hyperparameters, I utilized 'english' stop words for my vectorizer, and 20 topics for NMF. The high number of topics enabled me to find topics that were meaningful and distinguishable. While no formal analysis was conducted to compare price to these various topic frequency, I plotted both of these over a day to day timeframe and found some indications of correlation. These charts provide inspiration for future analysis, potentially in the form of a time-series regression.

## Tools
**Numpy and Pandas** - Data Preparation  
**Snscrape** - Python Scraping library that enables webscraping for social networking services (SNS)   
**Scikit-learn** - Python Machine Learning library that provides NLP Modeling      
**NLTK** - Natural Language Tool Kit   
**Matplotlib / Seaborn / Textacy** - Data visualization tools 

## Communication
After conducting my analysis, I shared my findings with my cohort via this [presentation](https://github.com/mkamel96/Classification-Project/blob/main/Classification%20Final/Classification%20Project.pdf).
