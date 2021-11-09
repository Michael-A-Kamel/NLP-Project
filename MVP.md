Hello Polychain Capital,

I'm writing to update you all on the progress of the twitter sentiment analysis algorithm, in the form of an MVP. This is a key step in the process, as it enables me to examine whether my current trajectory seems appropriate and effective.

For a first attempt at such an algorithm, I chose to look at a crypto asset that is almost entirely retail driven (as opposed to influenced by institutional backing). I hypothesize that retail crypto assets are more sentiment based, thus a better choice for this type of analysis.

The asset I chose for this first attempt is Catgirl Coin, a fairly new crypto asset with retail focus. After scraping about 10,000 tweets from the twitter search "#CATGIRLCOIN", filtering for tweets with 3+ likes, preprocessing & tokenizing the tweets, and running a NMF topic modeling on the body of tweets, here are the topics that were generated:

![Screen Shot 2021-11-08 at 6 58 18 PM](https://user-images.githubusercontent.com/73137112/140837988-343582cf-e26a-472b-833d-ff29f4202323.png)

Without context, these topics don't seem to distinguish tweets very well or hold much weight. However, we need to consider the goal of the project: predicting asset price based on these tweets. Therefore, the following steps need to be considered:

- Grouping tweets by time frame(day), so that each document of our corpus contains more content
- Considering additional EDA, such as including "catgirlcoin" in our stop words
- Look to sentiment analysis as oppose to topic modeling, for more clear tweet labeling (such as ones used here https://www.sciencedirect.com/science/article/abs/pii/S187775031100007X)

Once that is done, the following also needs to be completed:

- Adding this NLP modeling output to a predictive pricing model
- Running similar process for 2 additional crypto assets, for semi-retail (Cardano) and fully institutional (Ethereum)

These steps will enable us to see if any form of topic or sentiment analysis can prove helpful in predicting a crypto assets price.

Thank you, and look forward to future insights.

Best,

Michael
