Dear Polychain Capital,

Before diving in to the scope of this project, I wanted to begin by thanking you for the opportunity to work on such an exciting undertaking. The world of crypto is filled with mystery and room for growth, and I hope to contribute to your ecosystem in a meaningful manner.

To understand the objective of this project, let's first review this key finding from PWC regarding crypto hedge funds:

"The median crypto hedge fund returned +128% in 2020 (vs +30% in 2019). The median best performance strategy in 2020 was discretionary long only (+294%) followed by discretionary long-short (+129%), multi-strategy (+114%) and quant (+72%)."

While it is apparent that crypto as a whole has done exceptionally well in past years, it seems as though discretionary strategies are outperforming quant strategies by a significant margin. Furthermore, it seems as though discrentionary strategies are less commonly used:



Below, you will find a high-level blueprint of the analysis, including the purpose of the analysis, the data being considered, and some of the tools I will use. Happy to clarify any of the below further on a call.

## **Purpose of Model** - Predict Crypto Price Movement Based on Twitter Activity

My goal here is to develop a model that can detect whether a transaction on the Bitcoin Network is associated with ransomware or criminal activity.

## **Data Being Examined** - Scraped Tweets with relevant hashtags and hourly crypto price movement

I will be using the following dataset: https://archive.ics.uci.edu/ml/datasets/BitcoinHeistRansomwareAddressDataset# , which incorporates different features per Bitcoin transaction, and has labeled them with a criminal organization, or "white," as a clean transaction (as far as we know).

## **Data Analysis Tools**

**Pandas** - DataFrame tool that will enable me to organize data prior to analysis  
**Scikit-learn** - Python Machine Learning library that will enable me to run linear regressions  
**Matplotlib / Seaborn / Tableau** - Data visualization tools that will enable me to present the results in a clear manner  

## **First Deliverable** - MVP Goal
On Tuesday (11/9) at 6 pm EST, I will deliver my first pass at this model, including a baseline analysis.

Thank you for your trust in me, and I look forward to working together in the coming weeks.

Best,

Michael
