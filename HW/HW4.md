# Homework 4 - Exploring Social Networks
**Due:** In 2 weeks
 
Read through the entire assignment before starting.  

## Assignment 

This assignment will have you investigate the [friendship paradox](http://en.wikipedia.org/wiki/Friendship_paradox) on Facebook and Twitter, which says "most people have fewer friends than their friends have, on average." 

Write a report that answers and *explains how you arrived at the answers* to the following questions. 

**Reminder about Programming Tasks:** For several of the programming tasks this semester, you will be asked to write code to operate on 100s or 1000s of data elements.  If you have not done this type of development before, I *strongly encourage* you to start small and work your way up.  Especially when you are using new tools or APIs, start on a small test dataset to make sure you understand how to use the tool and that your processing scripts are working before ramping up to the full set. *This will save you an enormous amount of time.*

### Q1. Friendship Paradox on Facebook

Determine if the friendship paradox holds for a user's Facebook account. *(This used to be more interesting when you could more easily download your friend's friends data from Facebook.  Facebook now requires each friend to approve this operation, effectively making it impossible.)* 

[hw4-friend-count.csv](hw4-friend-count.csv) contains a user's friends' names and number of friends they each have. 

*Q: What is the mean, standard deviation, and median of the number of friends that the user's friends have?*  

Create a graph with the number of friends that each of the user's friends has, sorted by decreasing number of friends.  The friend with the most friends should be on the left side of the graph and the friend with the least friends should be on the right side of the graph. The friends don't need to be labeled with their names on the x-axis, just 1, 2, 3, ... *n* is fine.  Include the user in the graph in the appropriate sorted position (count the number of their friends) and label as *U*.

*Q: Does the friendship paradox hold for this user and their friends on Facebook?*

### Q2. Friendship Paradox on Twitter

Determine if the friendship paradox holds for your Twitter account. Since Twitter is a directed graph, use *followers* as the value you measure (i.e., "do your followers have more followers than you?").  

If you have less than 50 followers on Twitter, then you can do the analysis for another Twitter account and substitute the user you pick for *you* in the questions below.

*Q: What is the mean, standard deviation, and median of the number of followers that your followers have?*  

*Q: Does the friendship paradox hold for you and your followers on Twitter?*

You should use Twarc2 in Python to access the Twitter API to find a user's followers.  The code to access the Twitter API should be similar to [collect-tweets.py](../code/collect-tweets.py) from EC0.7, so you can use that as a starting place.

Other helpful references:
* [Labs for the Standard Product Track in Python](https://github.com/twitterdev/getting-started-with-the-twitter-api-v2-for-academic-research/blob/main/modules/6b-labs-code-standard-python.md) - look at the section headings to find the appropriate part to read
* [Twitter's User object model](https://developer.twitter.com/en/docs/twitter-api/data-dictionary/object-model/user) - explains the data structure returned from the Twitter API
* [process-tweets.py](../code/process-tweets.py) - from EC0.7, shows examples of accessing different parts of the data structure returned from the Twitter API

## Extra Credit

### Q3. 

Repeat Q2, but change *followers* to *following*.  

*Q: Are the people you are following following more people than you are?*

### Q4. 

Since Twitter is uni-directional, we can examine friendships, where someone you are following is also following you.

*Q: How many friendships do you have on Twitter?*  

List the usernames of those who have a bi-directional relationships with you. 
