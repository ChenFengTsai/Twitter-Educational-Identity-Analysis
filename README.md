# Twitter-Educational-Identity-Analysis
## Overview
* Processed 70 million tweets to analyze trending topics in education and identify user identity categories
* Applied Jaccard similarity to discover duplication patterns in tweet contents and analyze its characteristics
* Analyzed geographical and timeline progression in topic like Florida Math Book Ban from influential users

## Tools
PySpark, GCP DataProc

## Executive Summary
This analysis report is to analyze the patterns of tweets in education category. There are some points to be highlighted. 
First, the most prolific twitterers in this category are sports related users, and after using the influential score as metrics, political entities and news oulets are two main influential source in the whole category, especially in K-12 Topic. 
Second, most of the tweets come from the main city in the US, and the ranking is consistent with population ranking. For geogrpahical progression in Florida Math Book Ban, there is an increasing trend from the east coast to the west coast.
Third, there are gaps between Decemebr to March, and the peaks happen at October. Reason behind this might be school semester system and election.
Fourth, ⅕ of the tweets in Florida Math Book Ban are duplicate.
In conclusion, tweets are credible source of information since it correctly points out the author identification and where the topics emerge and progress, and imply further inference of relationship with timeline. Furthermore, most of the tweets are unique, which makes it more credible.

## Methodology
Analyzing tweet data in education to discover patterns from multiple aspects:
* Author Identification
  * To see who are the twitterers that post most about education and are most influential
  * Extract information about the top prolific twitterers to cateogrize their identification
  * Design metrics to calculate influential score for each twitterers and types of organizations
* Location Analysis
  * To see where are these tweets from and is their any patterns in these locations
  * Compare the distributions from country perspectives and city perspectives
  * Explore the geographical patterns by time using respective distribution plot
* Timeline Analysis
  * To see whether there are seasonality in these education tweets
  * Compare the aggregate tweet counts by month 
* Message Uniqueness Analysis
  * To explore whether people are just copying the same text
  * Using Jaccard similarity to extract duplication
  * Compare the duplication between each types of twitterers

## Conclusion
* Author Identification:
 * Most of the prolific twitterers are related to sports
 * Twitterers with most influential effect are political entities, then social influencer
 * Those that tweet about K-12 are news and political entities
* Location Analysis
 * Most of the tweets aggregate in main city like New York, Chicago, Los Angelas
 * Topic like Florida Math Book Ban spreads from East to the West
* Timeline Analysis
 * There is a gap from December to March which does not have any tweets
 * There are peaks in Spring and Autumn
 * Reason might be semester system and election
* Message Uniqueness Analysis
 * 26262 duplicate out of 109509 tweets in Florida Math Book Ban
 * Most of the duplicate tweets are not about the topic except political entities

## Actionable Recommendayions
* To improve the analysis result, I think a better text mining method will work, such as not only considering one word token search, but using ngram words to filter topics.
* Finding better topic could better analyze the geographical spread in tweets, which can make the analysis more clear and more logical.
* Many tweets have the same user_id but different profile, which could be problem. This time I use max function to extract one user name for each user id. Next time, I should use create time to find themost recent identity.
* User location variable I pick might not be a good indicator to find where exactly the post is made since the users might move; however, using place information of the tweet does not work either since there are lots of missing value. Finding a better way to profile their location could be a huge improvement in location analysis.

