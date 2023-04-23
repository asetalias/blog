+++
title = 'A Look Inside the Twitter Recommendation Algorithm'
slug = 'twitter-algorithm'
cover.image = 'images/twitter-banner.png'
date = "2023-04-19T09:23:23"
author = 'Raghav Sethi'
tags=['DevOps', 'Open Source', 'Machine Learning']
categories =['Open Source', 'ML']
description = 'How does Twitter decide what kind of tweets do you get to see on your feed?'
disableComments = false
+++

Twitter is one of the most popular social media platforms today, with millions of active users worldwide. One of the key features of Twitter is its recommendation algorithm, which suggests content to users based on their interests and behaviors. In an effort to increase transparency and promote collaboration, Twitter made their recommendation algorithm open source. In this blog post, we will discuss the benefits of open-sourcing the algorithm and how it works.

## About The Algorithm

Twitter's recommendation algorithm is based on machine learning and uses a variety of inputs to make recommendations. The algorithm uses a combination of supervised and unsupervised learning techniques to analyze user behavior and make personalized recommendations.

The code for the algorithm is written in Python and uses a number of libraries, including TensorFlow and Scikit-learn. The algorithm is trained on a large dataset of user behavior, which includes information such as tweets liked, retweeted, and replied to, as well as the user's location, language, and device type.

The algorithm uses a neural network to learn patterns and trends in the user behavior data. The neural network consists of multiple layers of nodes, with each layer performing a different type of computation. The input layer of the neural network takes in the user behavior data, and the output layer produces a set of recommendations for the user.

## Benefits of Open-Sourcing the Algorithm

By making their recommendation algorithm open source, Twitter is allowing researchers and developers outside of the company to study and improve the algorithm. This promotes transparency and accountability, as it allows the public to see how the algorithm works and how it makes recommendations. Additionally, open-sourcing the algorithm allows for collaboration between Twitter and other companies or individuals who are interested in improving the algorithm. This can lead to better recommendations and a better user experience for Twitter users.

## How are Tweets ranked?

The algorithm works by creating a pipeline where the best 1500 tweets are selected from a pool of hundreds of millions of tweets. This generally applies to the "For You" feed where 50% In-Network Tweets and 50% Out-of-Network Tweets are displayed to the user, although recent updates now only allow verrified accounts to appear on the For You timeline.

For In-Network tweets, a model called **Real Graph** is used, which tries to predict the probability of interaction/engagement between the 2 users. It uses a scoring system, where if the Real Graph score between 2 users is higher, then more tweets will from one user will be included in the other user's feed.

For Out-of-Network tweets it's a slightly more complicated problem since finding relevant tweets would be trickier. To solve this problem Twitter has developed a graph processing engine called **GraphJet** which records and analyses interaction between users and tweets. The main 3 questions asked here are :-


-*What Tweets did the people I follow recently engage with?*\
-*Who likes similar Tweets to me, and what else have they recently liked?*\
-*What Tweets and Users are similar to my interests?*

![image](/blog/images/twitteralgochart.png#center)


## Multiplier System

There is also a multiplier system where the reachability of tweets is impacted by certain parameters such as likes, replies, etc. Likes have a multiplier boost of 30 times and retweets have a boost of 20 times. An extensive list of these multiplier levels can be found in the code attatched below. This is a great way to get insight into how a tweet can achieve better reachability and visibility. 

It should be kept in mind though that offensive of NSFW tweets might not rank well, and even spamming multiple hashtags might get decrease the visibility of a tweet, but trending topics also might get you a small boost at the same time.



```scala  

  //snippet from the source code

  30: optional double langEnglishUIBoost = 0.3
  // tweet language is english, UI language is not
  31: optional double langEnglishTweetBoost = 0.7
  // user language differs from tweet language, and neither is english
  32: optional double langDefaultBoost = 0.1
  // user that produced tweet is marked as spammer by metastore
  33: optional double spamUserBoost = 1.0
  // user that produced tweet is marked as nsfw by metastore
  34: optional double nsfwUserBoost = 1.0
  // user that produced tweet is marked as bot (self similarity) by metastore
  35: optional double botUserBoost = 1.0

  // An alternative way of using lucene score in the ranking function.
  38: optional bool useLuceneScoreAsBoost = 0
  39: optional double maxLuceneScoreBoost = 1.2

  // Use user's consumed and produced languages for scoring
  42: optional bool useUserLanguageInfo = 0

  // Boost (demotion) if the tweet language is not one of user's understandable languages,
  // nor interface language.
  43: optional double unknownLanguageBoost = 0.01

  // Use topic ids for scoring.
  // Deprecated in SEARCH-8616.
  44: optional bool deprecated_useTopicIDsBoost = 0
  // Parameters for topic id scoring.  See TopicIDsBoostScorer (and its test) for details.
  46: optional double deprecated_maxTopicIDsBoost = 3.0
  47: optional double deprecated_topicIDsBoostExponent = 2.0;
  48: optional double deprecated_topicIDsBoostSlope = 2.0;

  // Hit Attribute Demotion
  60: optional bool enableHitDemotion = 0
  61: optional double noTextHitDemotion = 1.0
  62: optional double urlOnlyHitDemotion = 1.0
  63: optional double nameOnlyHitDemotion = 1.0
  64: optional double separateTextAndNameHitDemotion = 1.0
  65: optional double separateTextAndUrlHitDemotion = 1.0  
```



## Does Your Follower-Following Ratio Play a Role?

As suggested in the code attatched below, if a user is following way more users than the number of people following them, their tweets may get a nerf in terms of ranking. The quality of users you interact with also plays a role, as interacting with bots, spam accounts or accounts with lower rankings might also get you a demotion. This entire system does play out almost like an ELO ranking system at times!

```scala
 /**
   * reduce pagerank of users with low followers but high followings
   */
  def adjustReputationsPostCalculation(mass: Double, numFollowers: Int, numFollowings: Int) = {
    if (numFollowings > threshAbsNumFriendsReps) {
      val friendsToFollowersRatio = (1.0 + numFollowings) / (1.0 + numFollowers)
      val divFactor =
        scala.math.exp(
          constantDivisionFactorGt_threshFriendsToFollowersRatioReps *
            (friendsToFollowersRatio - threshFriendsToFollowersRatioUMass) *
            scala.math.log(scala.math.log(numFollowings))
        )
      mass / ((divFactor min maxDivFactorReps) max 1.0)
    } else {
      mass
    }
  }


```

## How Much Does Your Content Matter?

You can also increase the chances of your tweet being seen by including media like images or videos. Additionally, tweeting about current news or events can give your tweet a boost as Twitter usually highlights the most recent and pertinent content.

On the flip side, there are some actions that can downgrade the ranking of your tweet. Posting a tweet that contains no text or solely a URL is likely to be deprioritized. Likewise, tweeting only your name without any other content will probably not gain much visibility.

To ensure your tweet ranks high, it's essential to focus on incorporating engaging and relevant content, attaching media where possible, and keeping up-to-date with current events and trends. Avoid tweeting with limited content since they are prone to being deprioritized in the rankings.

```scala
if (scoringData.tweetHasTrendsBoostApplied) {
 boostDetails.add(Explanation.match(
     (float) params.tweetHasTrendBoost, "[x] Tweet has trend boost"));
}

if (scoringData.hasMedialUrlBoostApplied) {
 boostDetails.add(Explanation.match(
     (float) params.tweetHasMediaUrlBoost, "[x] Media url boost"));
}

if (scoringData.hasNewsUrlBoostApplied) {
 boostDetails.add(Explanation.match(
     (float) params.tweetHasNewsUrlBoost, "[x] News url boost"));
}

boostDetails.add(Explanation.match(0.0f, "[FIELDS HIT] " + scoringData.hitFields));

if (scoringData.hasNoTextHitDemotionApplied) {
 boostDetails.add(Explanation.match(
     (float) params.noTextHitDemotion, "[x] No text hit demotion"));
}

if (scoringData.hasUrlOnlyHitDemotionApplied) {
 boostDetails.add(Explanation.match(
     (float) params.urlOnlyHitDemotion, "[x] URL only hit demotion"));
}

if (scoringData.hasNameOnlyHitDemotionApplied) {
 boostDetails.add(Explanation.match(
     (float) params.nameOnlyHitDemotion, "[x] Name only hit demotion"));
}

if (scoringData.hasSeparateTextAndNameHitDemotionApplied) {
 boostDetails.add(Explanation.match((float) params.separateTextAndNameHitDemotion,
     "[x] Separate text/name demotion"));
}


```

## Some Weird Stuff

In the initial commit, there was some code which categorised users into Democrats, Republicans, and who is Elon and who is **not Elon**. Elon Musk's name was found in the source code. Although this solely appears to be for data collection purposes, it's still kind of funny seeing Elon's name being individually coded in to collect analytics.

```scala

 "author_is_elon",
      candidate =>
        candidate
          .getOrElse(AuthorIdFeature, None).contains(candidate.getOrElse(DDGStatsElonFeature, 0L))),
    (
      "author_is_power_user",
      candidate =>
        candidate
          .getOrElse(AuthorIdFeature, None)
          .exists(candidate.getOrElse(DDGStatsVitsFeature, Set.empty[Long]).contains)),
    (
      "author_is_democrat",
      candidate =>
        candidate
          .getOrElse(AuthorIdFeature, None)
          .exists(candidate.getOrElse(DDGStatsDemocratsFeature, Set.empty[Long]).contains)),
    (
      "author_is_republican",
      candidate =>
        candidate
          .getOrElse(AuthorIdFeature, None)
          .exists(candidate.getOrElse(DDGStatsRepublicansFeature, Set.empty[Long]).contains))

```

## Conclusion

In conclusion, Twitter's open-source recommendation algorithm is a significant step towards transparency and collaboration in the field of machine learning. By allowing researchers and developers outside the company to study and improve the algorithm, Twitter is promoting accountability and trust in their platform. The algorithm uses a combination of supervised and unsupervised learning techniques to analyze user behavior and provide personalized recommendations. The algorithm also utilizes a variety of features and parameters such as Real Graph and GraphJet to rank tweets and ensure optimal visibility and reachability. Additionally, the multiplier system provides insight into how tweets can achieve better reachability and visibility. Overall, the open-source recommendation algorithm is a valuable resource for developers, researchers, and the general public who are interested in understanding and improving Twitter's recommendation system.
