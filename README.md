# Twitter NLP Topic Modeling Analysis for Crypto Hedge Fund
Michael Kamel

## Abstract
According to [PWC](https://www.pwc.com/gx/en/financial-services/pdf/3rd-annual-pwc-elwood-aima-crypto-hedge-fund-report-(may-2021).pdf), crypto hedge funds had a median return of 128% in 2020, up from 30% in 2019. In terms of specific strategies, discretionary long only strategies generated 294% returns, while quantitative strategies generated 72% returns. My project is targeted at discretionary long strategies. Specifically, the goal of my project is to empower these hedge fund's research teams by providing them with analysis of retail investor opinion through Twitter NLP Topic Modeling. Via NMF models, I was able to distinguish some meaningful groupings of tweets for research analysis, with some indication of correlation between price and topic prevalence.

## Design
The idea for this project came from the PWC article I read as well as the general state of crypto currency at the moment. The article cites statistics that show a great deal of success in regards to discretionary investing, while relatively less success with quantitative investing. In terms of crypto currency, it’s no secret that hype and public sentiment have a relationship with the price of crypto assets. Take a look at Dogecoin, originally created as a joke, that now has a market cap of $33.8 billion. It seems clear to me that there is more to evaluating a crypto currency than conducting a technical analysis or examining its value proposition. It seems evident that a crypto asset's view in the public eye is a key determining factor in its price. Therefore, this project is designed to build an NLP model that can scan and analyze ideas from Twitter in a manner that is helpful to discerning public opinion. From there, researchers can both view the prevalence of certain groupings of tweets (such as optimistic tweets) and potentially try to utilize these groupings as features in a time-series linear regression model.


## Data
I utilized Snscrape, a Python Scraping Library geared toward social networking services (SNS), to scrape 500K tweets containing #Solana. I selected to model tweets regarding Solana as this asset falls in an interesting middle-ground between institutional focus and retail support. From there, I filtered the data to only include tweets with 3 or more likes, and pre-processed the tweets to be ready for tokenization (lower-case, no punctuation, turning emojis to text, etc). Lastly, I tokenized the cleaned tweets using NLTK, finalizing the preparation needed for modeling.

## Algorithms
TF-IDF was most suited for vectorization for this problem, as there is plenty of repetition amongst crypto tweets (naming of the various crypto assets, for instance). In terms of topic modeling, NMF was most suitable, as the documents were short, and there is naturally an emphasis on interpretability, given the use case (research). Both of these factors play into the strengths of NMF modeling. In terms of hyperparameters, I utilized 'english' stop words for my vectorizer, and I had the NMF model output 20 topics. After trial and error, I found that this high number of topics enabled me to find topics that were both meaningful and distinguishable. In particular, the 3 that caught my attention were Topic 2 - Coin Comparison (most commonly referring to Ethereum), Topic 4 - Optimism (most commonly using rocket emojis), and Topic 13 - Anticipation (most commonly using eye emojis).

While no formal analysis was conducted to compare Solana’s price to these various topic frequencies, I plotted both the price of Solana and the prevalence of these three topics over a day to day timeframe and found some indications of correlation. These charts provide inspiration for future analysis, likely in the form of a time-series regression. Here is an example of one below (you can find all three in my presentation):

![Topic 13   Solana Price](https://user-images.githubusercontent.com/73137112/149975613-4f77878d-f8f4-4953-9fa6-ff28a4a3d1a5.png)

## Tools
**Numpy / Pandas** - Data Preparation  
**Snscrape** - Python Scraping library that enables web scraping for social networking services (SNS)   
**Scikit-learn** - Python Machine Learning library that provides NLP Modeling      
**NLTK** - Natural Language Toolkit   
**Matplotlib / Seaborn / Textacy** - Data visualization tools 

## Communication
After conducting my analysis, I shared my findings with my cohort via this [presentation](https://github.com/Michael-A-Kamel/NLP-Project/blob/main/NLP%20Project%20Presentation.pdf).
