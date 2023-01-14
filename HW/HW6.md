# Homework 6 - Analyzing Disinformation Domains
**Due:** In 2 weeks

Read through the entire assignment before starting.  

## Assignment

This assignment will have you will investigate domains that were determined to be sharing disinformation about COVID-19. (*Note that this assignment may result in fewer relevant tweets the farther out from 2020 it is attempted.*)

Write a report that answers and *explains how you arrived at the answers* to the following questions.  

### Data Source

[hw6-domains.csv](hw6-domains.csv) - 346 domains that were determined to be publishing false Coronavirus information, gathered by [NewsGuardTech's Coronavirus Misinformation Tracking Center](https://www.newsguardtech.com/special-reports/coronavirus-misinformation-tracking-center/) as of October 29, 2020 ([archived version](http://web.archive.org/web/20201029234552/https://www.newsguardtech.com/coronavirus-misinformation-tracking-center/))

* fields: domain, country, notes

### Q1 - Collect and Analyze New Tweets

Use twarc's `search_recent()` to request 100 tweets that contain links from 25 of the domains that appear in the dataset. It's ok if you do not find 100 recent tweets for each domain.
* Hint: You can set up your query as `"url:" + domain + " lang:en"` to search for English language tweets that contain links with the given `domain`.

I would recommend writing a separate script to collect tweets and write out the information to JSONL file(s) and a separate script that reads in the files later for processing (similar to the previous examples `collect-tweets.py` and `process-tweets.py`).

*Q: How many total tweets did you gather?*

*Q: How many tweets did you discover for each domain?*  Create a table showing the number of tweets for each domain.

*Q: How many different authors posted tweets?*  

*Q: Who were the top 10 authors in terms of tweets in the dataset?*

*Q: Who were the top 10 authors in terms of followers?*

See the earlier `process_tweets.py` example for how to access the username of the author of each tweet and their number of followers.

## Extra Credit

### Q2 - Disinformation Games 

There have been several online games created to educate people about disinformation and how it spreads on social media.  Play one of the games at https://fakey.osome.iu.edu/, https://www.getbadnews.com, or https://goviralgame.com.  Write a paragraph about your experience and some lessons you learned by playing the game. Take some screenshots as you play to include in your report.

### Q3 - Tweet Text Analysis 

Investigate the text of the tweets you collected in Q1 and report on any interesting findings.  Here are some example questions you could look at:
* What were the most common terms?
* How many tweets contained the most common terms?
* How many times was a single tweet repeated?

What insights did you gain?  What could be some avenues for further investigation?

### Q4 - Archived Domains 

For each domain in the dataset, check the archival status of the domain's main webpage using MemGator. 

Save a data file that contains each domain name, datetime of its first memento, datetime of its last memento, and its total number of mementos. 

Note that some of the main webpages should have at least 1 memento because the Internet Archive has created an Archive-It collection of these (see https://archive-it.org/collections/13559). Though, this collection was created in March 2020 and the list is continually being updated by NewsGuardTech.

Create a scatterplot of domain vs. datetime of the first memento and last memento (x-axis), sorted by the datetime of the first memento.  This should look similar to this [chart of URIs vs. memento datetimes](https://3.bp.blogspot.com/-8vNC-7UraiQ/U43lwAC0pSI/AAAAAAAAAE4/1IyHbXH9CKQ/s1600/mementosScatterDmoz.png), but with only the first and last dot on each row plotted (since you're only plotting the datetimes of the first and last mementos).
