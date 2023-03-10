# Homework 8 - Clustering
**Due:** In 2 weeks

## Assignment

The goal of this assignment is to cluster Twitter accounts based on the content of their last 100 (or so) tweets.

Write a report that answers and *explains how you arrived at the answers* to the following questions. 

**Tips for Completing this Assignment:**
* First, read the entire assignment before starting.
* Your first reference should be the Module 12 slides, class Colab notebook, and *Programming Collective Intelligence* book and [Chapter 3 code](https://github.com/arthur-e/Programming-Collective-Intelligence/tree/master/chapter3).  *Don't start with a Google search.*

### Q1 - Find Popular Twitter Accounts
Generate a list of 100 popular accounts on Twitter.  The accounts must be verified and have > 10,000 followers.  For example:
* [weiglemc](https://twitter.com/weiglemc) - not verified, 685 followers - *don't include*
* [wnba](https://twitter.com/WNBA) - verified (blue/yellow checkmark), 804.1K followers - *could include*

See [Twarc API user_lookup](https://twarc-project.readthedocs.io/en/latest/api/client/#twarc.client.Twarc.user_lookup), [GET users/lookup](https://developer.twitter.com/en/docs/accounts-and-users/follow-search-get-users/api-reference/get-users-lookup), and [User object](https://developer.twitter.com/en/docs/twitter-api/data-dictionary/object-model/user) for details on obtaining this information for a set of accounts.  

You may also generate this information manually by visiting individual account pages. 

Because we're trying to cluster the accounts based on the text in their tweets, you should choose several sets of accounts that are similar (political, tech, sports, etc.) to see if they'll get clustered together later.

Save the list of accounts (screen_names), one per line, in a text file named `accounts.txt` and upload to your GitHub repo.

*Q: How did you choose to collect the accounts?*

*Q: What topics/categories do the accounts belong to?  You don't need to specify a grouping for each account, but what general topics/categories will you expect to be revealed by the clustering?*

### Q2 - Create Account-Term Matrix

Before we can run the clustering code from the PCI book, we have to build an account-term matrix (like the blog-term matrix in the Module 12 slides).  We will consider all of the tweets from a single account to be the same as a "blog" from our class examples.

The PCI book provided code for creating the blog-term matrix given a list of blog feeds.  I've provided similar code for you in this repo:
* [tweetparser.py](tweetparser.py) - This is similar to the feedparser library mentioned on pg. 31.  It contains two functions used by `generatetweetvector.py`:
    * `setup_api(filename)` - set up and return a Twitter API object, `filename` is the file containing your API keys
    * `parse(api, screen_name, num_tweets=100)` - use Twarc2 to download about 100 tweets (excluding replies and retweets) from the timeline of the `screen_name` account and return a dictionary with the following structure:   
    `{'screen_name': screen_name, 'tweets': [tweet1, tweet2, ...]}`

* [generatetweetvector.py](generatetweetvector.py) - This is similar to [`generatefeedvector.py`](https://github.com/arthur-e/Programming-Collective-Intelligence/blob/master/chapter3/generatefeedvector.py) described on pgs. 31-33 in PCI.  It contains main code and two functions:
    * `getwordcounts(api, screen_name)` - calls `parse()` from `tweetparser.py` and returns the screen_name and a dictionary of word counts appearing in that account's tweets, almost exactly like `getwordcounts()` in our examples
    * `getwords(tweet)` - takes a tweet and returns a filtered list of words, similar to `getwords()` in our examples, but with some added filtering:
        * removes URLs
        * removes screen names (starting with @)
        * splits words by non-alphabetic characters (and thus removes any numbers and symbols)
        * removes any words < 3 characters or > 15 characters
        * lowercases all words

`generatetweetvector.py` requires that you have `accounts.txt` (from Q1) and `tweetparser.py` located in the same folder.  

`generatetweetvector.py` will ***not work out-of-the-box***.  
* First, on line 51, you'll need to insert the path to your Twarc config file.
* Second, instead of creating an account-term matrix for every term in the tweets, I only want the 500 most popular terms that are not stopwords.  ***You will need to write this code.***  To help with this, I've added a `sumcounts` dict that holds the words and frequency of those words over all accounts and a blank list `popularlist` where you should store the 500 most frequent non-stopword terms. On line 88, you'll see a section labeled `# BEGIN YOUR CODE BLOCK`. This is where you'll add your code.

Once complete, `generatetweetvector.py` will produce two files that you need to upload to your GitHub repo:
* `popularlist.txt` - the list (one per line) of the 500 most frequent terms in the tweets
* `tweetdata.txt` - the generated account-term matrix

Once `tweetdata.txt` has been generated, you can use it in place of `blogdata.txt` in the example code to complete the remaining parts of this assignment.

*Q: Explain the general operation of generatetweetvector.py and how the tweets are converted to the account-term matrix.*

*Q: Explain in detail the code that you added to filter for the 500 most frequent non-stopword terms.*

*Q: Do the 500 most frequent terms make sense based on the accounts that you chose?*

### Q3 - Create Dendrogram
Create an ASCII dendrogram *and* a JPEG dendrogram that uses hierarchical clustering to cluster the most similar accounts (see Module 12, slides 21, 23).  Include the JPEG in your report and upload the ASCII file to GitHub (it will be too unwieldy for inclusion in the report).

*Q: How well did the hierarchical clustering do in grouping similar accounts together?  Were there any particularly odd groupings?*

### Q4 - Cluster using k-Means
Cluster the accounts using k-Means, using `k`=5,10,20 (see Module 12, slide 37).  For each value of `k`, create a file that lists the accounts in each cluster and upload to your GitHub repo.  

*Q: Give a brief explanation of how the k-Means algorithm operates on this data.  What features is the algorithm considering?*

*Q: How many iterations were required for each value of `k`?*

*Q: Which `k` value created the most reasonable clusters?  For that grouping, characterize the accounts that were clustered into each group.*

### Q5 - Create MDS Image

Use MDS to create a JPEG of the accounts (see Module 12, slide 50).  Include the JPEG in your report. 

*Q: How many iterations were required?*

*Q: How well did the MDS do in grouping similar accounts together?  Were there any particularly odd groupings?*

## Extra Credit

### Q6 - Generate Nicer Dendrogram (not ASCII art)  

Generate the dendrogram figure from Q3 using [scipy's dendrogram](https://docs.scipy.org/doc/scipy/reference/generated/scipy.cluster.hierarchy.dendrogram.html) or [plotly's create_dendrogram](https://plotly.com/python/dendrogram/). The clustering should be the same as what you get in Q3.

### Q7 - Generate Nicer MDS Image  

Generate the MDS figure from Q5 as a scatterplot using regular Python graphing libraries or Vega-Lite/D3.  Plot the labels (could be in addition to the points or in place of the points) or allow the user to mouse-over the points and display the labels (i.e., tooltips). The figure won't look exactly like Q5 since the initial placement is random, but it should be similar. 

### Q8 - Generate Account-Term Matrix with TF-IDF   

Re-generate the account-term matrix but this time process the terms using proper TF-IDF calculations instead of the hack discussed on slide 12 (p. 32).  Use the same 500 terms, but this time replace their frequency count with TF-IDF scores (similar to as computed in HW3). Document the code, techniques, methods, etc. used to generate these TF-IDF values.  Upload the new account-term matrix file to GitHub.
*  For this IDF computation, you can use the tweets you gathered in Q1 as your corpus (instead of searching Google for each term).  Treat the set of tweets from each account as a single document.

Then re-do Q3 with the new matrix.  Compare and contrast the resulting dendrogram with the dendrogram from Q3.

Note: Ideally you would not reuse the same 500 terms and instead would come up with TF-IDF scores for all the terms and then choose the top 500 from that list, but I'm trying to limit the amount of work necessary.
