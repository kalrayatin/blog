---
layout: post
title: "TweetFeed - A Bot"
author: Yatin Kalra, Yash Malani
date:   2021-02-01 12:12:12 +0530

categories: [Productivity]
tags: [Twitter, Bot] 
comments: true

---

### Introduction
Counted among Twitter’s 270+ million dynamic clients, there are an untold number of bots. These were made by individuals with a heartbeat to tweet without human involvement. Some are helpful, others lovely, numerous impossible to miss. Bots, it ought to be stated, are the absolute most productive individuals from Twitter’s community.

Out of approximately 500 million [src: https://www.dsayce.com/social-media/tweets-day] tweets sent per day, many lacks the personal interest of a particular user in various ways.

TweetFeed is a python based project crafted for filtration of tweets for the end-user with the aim is to provide only personalized tweets to read for end-user using single or multiple hashtags.

For Example, A person P1 has 10k following, he/she got fed up with all the tweets prevailing in feed, but only want to see stuff published by following related to something related to #hashtag. Now by using TweetFeed, he can buckle up and get only the tweets related to hashtag.


### Python Script for TweetFeed

**Importing Libraries**
![Figure 1 — End User’s Tweet mentioning TweetFeed and hashtag](https://github.com/kalrayatin/blog/blob/main/assets/img/socialengineering.jpg?raw=true)
**2. Authentication**
![Figure 2 — TweetFeed’s Reply of Personalized Tweets by Following](https://github.com/kalrayatin/blog/blob/main/assets/img/socialengineering.jpg?raw=true)

*Here we are using tweepy library to use Twitter API via consumer key, consumer secret key, access token, and access token secret generated in https://developer.twitter.com/en*

**3. Retrieve all the tweets of followings and filter out the personalized one.**
<script src="https://gist.githubusercontent.com/yash2806/972e41b2c8b4bfbfcb4296d923088edb/raw/2149636b9f9369760122e5cc932151675a370099/TweetFeed.py">
</script>

*Here we are searching tweets for following accounts with filtering based on date of posting and #hashtag and return them in the form of array containing all personalized tweets*

**4. Store and retrieve last mentioned ID**
*Here we are using Last Mentioned ID concept to make the code differentiate between the previous mentions and latest mentions by storing the ID for previous mention in last_id.txt. In other words, to prevent the code from getting all the mentions again and again, and re-sending all the tweets all over again.*
**5. Feed the Tweets to end-user**
*Here we are taking the latest mention after last mentioned ID, and then Filtering out the hashtag from the mentioned tweet and getting the filtered array by calling tweetFunc() function. Finally, we will be sending the personalized tweets to the end-user in form of reply.*

### Conclusion

<p style="color: red;"><strong>TweetFeed Bot can be very useful for a person who gets panic or fed up by watching irrelevant posts in feed. This bot can make his/her life somewhat easy.</strong> </p>

**References:**

[https://developer.twitter.com/en/docs/twitter-api](https://developer.twitter.com/en/docs/twitter-api)
[https://www.youtube.com/watch?v=W0wWwglE1Vc](https://www.youtube.com/watch?v=W0wWwglE1Vc)

**Find the full Python code in Github Repo, Click [https://github.com/yash2806/TweetFeed](here)**

