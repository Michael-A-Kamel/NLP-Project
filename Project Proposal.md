Dear Polychain Capital,

Before diving into the scope of this project, I wanted to begin by thanking you for the opportunity to work on such an exciting undertaking. The world of crypto is filled with mystery and room for growth, and I hope to contribute to your ecosystem in a meaningful manner.

To understand the objective of this project, let's first review this key finding from [PWC](https://www.pwc.com/gx/en/financial-services/pdf/3rd-annual-pwc-elwood-aima-crypto-hedge-fund-report-(may-2021).pdf) regarding crypto hedge funds:

"The median crypto hedge fund returned +128% in 2020 (vs +30% in 2019). The median best performance strategy in 2020 was discretionary long only (+294%) followed by discretionary long-short (+129%), multi-strategy (+114%) and quant (+72%)."

While it is apparent that crypto as a whole has done exceptionally well in past years, it seems as though discretionary strategies are outperforming quantitative strategies by a significant margin. Furthermore, it seems as though discrentionary strategies are less commonly used:

<img width="617" alt="Screen Shot 2021-11-03 at 4 52 01 PM" src="https://user-images.githubusercontent.com/73137112/140194368-e84fec53-55c2-420f-b8c5-cdfd74f4c997.png">

The goal of my analysis is to bridge the gap between discretionary and quant analysis, in order to provide crypto hedge funds with a more reliable avenue for investment decisions.

Below, you will find a high-level blueprint of the analysis, including the purpose of the analysis, the data being considered, and some of the tools I will use. Happy to clarify any of the below further on a call.

## **Purpose of Model** - Predict Crypto Price Movement Based on Twitter Activity

My goal here is to develop a model that can predict crypto price movement given tweets regarding the crypto asset. The idea is to train a model using only NLP sentiment analysis to predict hourly price movement.

If successful, this could be a vital feature to include in quant analysis, and potentially bridge the gap between discretionary and quant analysis by providing the framework to quantify sentiment.

## **Data Being Examined** - Scraped Tweets and Hourly Crypto Price 

I will gather my data by scrapping twitter for a given hashtag. These tweets will act as my features for my model. My target will be the hourly price of said crypto, gathered from a financial crypto website, such as https://coinmarketcap.com/.

## **Data Analysis Tools**

**Pandas** - DataFrame tool that will enable me to organize data prior to analysis  
**Snscrape** - Python Scraping library that enables webscraping for social networking services (SNS)   
**Scikit-learn** - Python Machine Learning library that will enable me to run linear regressions   
**Matplotlib / Seaborn / Tableau** - Data visualization tools that will enable me to present the results in a clear manner  

## **First Deliverable** - MVP Goal
On Tuesday (11/9) at 6 pm EST, I will deliver my first pass at this model, including a baseline analysis.

Thank you for your trust in me, and I look forward to working together in the coming weeks.

Best,

Michael
