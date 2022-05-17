# 2021 Canadian election polls based on Twitter Sentiment Analysis
The project has the objective of calculating weekly polls of the 44° canadian election based on the sentiment analysis that can be performed over the extraction of Twitter's comments.

Considerations:
- The analysis will be of tweets from 2021-07-22 to 2021-09-20 (60 days)
- The extraction of tweets will be based on pre-defined hashtags or keywords related to the canadian election
- It will be calculated for each tweet a sentiment (pos, neutral, neg) and a political party (only the 6 most relevant: liberal, conservative, democratic, bloc-quebecois, people, and green). 
- For the sentiment, we will be using sentiment analysis with the SentimentIntensityAnalyzer of the "vaderSentiment" package. 
- The calculation of each party's vote preference will be based on the "positive" sentiment of the tweets. The negative and neutral sentiment will not be considered in the vote preference.
- Each party label will be calculated based on the keywords found in the text of each twitter. For example, if a tweet contains the keywords: "liberal" and "Justin Trudeau", the function will associate that tweet to the liberal party. If a tweet text has comments on more than one party, the party that has more words will be preserved. If it is not possible to calculate the party with the text, the tweet will be discarded.
