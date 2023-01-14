# Unit 1 - Web Science and Web Architecture

Unit 1 consists of 6 modules:

* Module 1: Introduction to Web Science and Web Architecture
* Module 2: Introduction to Python
* Module 3: Introduction to InfoVis with R and Python
* Module 4: Measuring the Web
* Module 5: Archiving the Web
* Module 6: Searching the Web

# Module 1 

## Introduction to Web Science and Web Architecture

**Overview:** This module introduces the field of web science as an interdisciplinary study of the Web's properties, protocols, algorithms, and societal effects. We will cover an intro to web science, the structure and size of the Web, web architecture, and the HTTP protocol.  We will also look at hands-on methods to directly talk with web servers using wget, curl, and telnet.

**Relevance:** This module lays the foundation for the semester's study of web science, as it introduces the basic ideas and architecture of the web.

### Objectives

After completing this module, students will be able to

* List the main interdisciplinary components of web science.
* Describe the small world network phenomenon and how it relates to web science.
* Given a set of pages and their links, classify each page as part of the SCC, IN, OUT, Tendrils, Tubes, or Disconnected categories of the Bow-Tie Structure of the Web.
* Explain the difficulties in determining the size of the Web.
* Describe the operation of a web crawler.
* Describe the steps required to load a typical web page, in terms of application-layer (DNS, HTTP) networking operations required.
* Differentiate between a web resource and web representation.
* Demonstrate how to communicate with a web server using curl, wget, and telnet.
* Describe the different categories of HTTP response codes
* Explain how a web client knows what URI to request next upon receiving a response with a 3xx (redirection) status code.

### Reading Assignment

* James Hendler, Nigel Shadbolt, Wendy Hall, Tim Berners-Lee, and Daniel Weitzner, ["Web Science: An Interdisciplinary Approach to Understanding the Web"](https://cacm.acm.org/magazines/2008/7/5366-web-science/fulltext), *Communications of the ACM*, July 2008, Vol. 51 No. 7, Pages 60-69
* [What is Web Science?](http://www.youtube.com/watch?v=demjTp3A55A), YouTube video from Web Science Trust (5:55)

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 01 slides (PDF)](slides-pdf/Module-01-Web-Science-Architecture.pdf) | [Module 01 slides (PPTX)](slides-pptx/Module-01-Web-Science-Architecture.pptx)

### Discussion Question

Give some examples of how you have encountered web science in your daily life over the past month. What were some of the different disciplines involved?  Are there aspects of your experience with web science that you feel researchers should be studying more?

### Homework Assignment

Explore some of the tools that will be used during the course:

* [Twitter, twarc](getting-started/twitter-setup.md) - follow the instructions to set up your access to the Twitter API and isntall the twarc tool
* [Working with tweets](getting-started/working-with-tweets.md) - use the provided Python scripts to collect and process a small set of tweets
* [Memgator](getting-started/memgator.md) - follow the instructions to set up and test a local instance of the Memgator tool

### Summary

Module 1 introduced the field of web science as an interdisciplinary study of the Web's properties, protocols, algorithms, and societal effects. 

# Module 2

## Introduction to Python

**Overview:** This module introduces Python, the main programming language that we will use for homework assignments this semester. We will cover basic syntax, input/output, conditionals, functions, modules, error handling, command-line arguments, regular expressions, and web libraries. The web libraries, such as the requests library and Beautiful Soup will be essential in completing homework assignments later in the semester.

**Relevance:** This module is essential for the rest of the semester, introducing the Python language and useful libraries

### Objectives

After completing this module, students will be able to

* Explain the differences between Python and C/C++ syntax.
* Execute simple Python commands on a Linux server and in a Google Colab notebook.
* Describe the differences between a tuple, list, and dictionary.
* Write a Python program that accepts command-line arguments.
* Write a Python program that uses the requests library to access a webpage.
* Write a Python program that uses the BeautifulSoup library to extract all of the links in a webpage.

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 02 slides (PDF)](slides-pdf/Module-02-Python.pdf) | [Module 02 slides (PPTX)](slides-pptx/Module-02-Python.pptx)

The slides will reference this 
[Python Google Colab notebook](code/Mod02_Python.ipynb).

### Additional References

Intro to Python Links

* [Introduction to Python](http://introtopython.org/)
* [CS 1110: Introduction to Computing Using Python](http://www.cs.cornell.edu/courses/cs1110/2012fa/), Cornell University
* [A Gentle Introduction to Programming Using Python](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-189-a-gentle-introduction-to-programming-using-python-january-iap-2011/lectures/), MIT Open Courseware
* [CS 11 - Python track](http://courses.cms.caltech.edu/cs11/material/python/index.html), Cal Tech
* [Python in One Easy Lesson](http://www-cs-faculty.stanford.edu/~nick/python-in-one-easy-lesson/), Stanford

Reference Books

* [Python in a Nutshell](https://www.oreilly.com/library/view/python-in-a/0596001886/) - 3rd edition available [via ODU](https://go.oreilly.com/old-dominion-university//library/view/python-in-a/9781491913833/)
* [Learning Python](https://www.oreilly.com/library/view/learning-python-5th/9781449355722/) - 5th edition available [via ODU](https://go.oreilly.com/old-dominion-university/library/view/learning-python-5th/9781449355722/)

### Homework Assignment

* [Python lab exercises](code/Mod02_lab.ipynb) - The goal of this lab assignment is to give you experience writing Python code to accomplish common tasks, including using the requests and Beautiful Soup libraries. 
* [HW1 - Web Science Intro](hw/HW1.md)

### Summary

Module 2 introduced Python, the main programming language used for homework assignments this semester. We covered basic syntax and the use of libraries such as requests and Beautiful Soup.

# Module 3

## Introduction to Info Vis with R, Python

**Overview:** This module covers an introduction to principles of information visualization and the creation of effective charts of data. The module introduces examples of creation of charts with R and the ggplot2 library and with Python and the Seaborn and matplotlib libraries.

**Relevance:** Being able to create effective charts from data is an essential component of data science, and thus, of web science.

### Objectives

After completing this module, students will be able to

* Distinguish between categorical and ordered attributes.
* Explain how marks and channels are related.
* Distinguish between the identity channel type and the magnitude channel type and indicate which channels belong to each type.
* Distinguish between the principles of expressiveness and effectiveness in visual encoding.
* List the channels for ordered attributes in order from most effective to least effective.
* Explain how the concepts of express, separate, order, and align all relate to arranging tabular data.
* Differentiate between line charts and bar charts and explain when each is appropriate.
* Explain how the boxplot idiom can characterize a distribution.
* Use R to create a bar chart, line chart, and scatterplot.
* Use Python charting libraries to create a bar chart, line chart, and scatterplot.

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 03 slides (PDF)](slides-pdf/Module-03-InfoVis.pdf) | [Module 03 slides (PPTX)](slides-pptx/Module-03-InfoVis.pptx)

The slides will reference 

* [InfoVis in R Colab notebook](Mod03_InfoVis_R.ipynb)
* [InfoVis in Python Colab notebook](Mod03_InfoVis_Python.ipynb)

### Discussion Question

Describe a recent visualization that you found interesting or compelling.  If it was online and is still publicly available, include the URI. What visualization idiom (or idioms) did it use?  Did you gain any insights, or learn anything new, from the visualization?

### Summary

Module 3 introduced principles of information visualization and chart making. 

# Module 4

## Measuring the Web

**Overview:** This module explores how researchers have studied the size of the web and how much the web changes over time (the dynamics of the web). The concepts of link rot and content drift are introduced.

**Relevance:** Understanding the size and scope of the web is essential to understanding the impact that the web has had on society. It is impossible to know the exact size of the web, but researchers have developed techniques to estimate it.

### Objectives

After completing this module, students will be able to

* Characterize the growth of the Web during the 1990s.
* Explain what it means that some web characteristics exhibit a power law distribution.
* Explain how researchers use search engines to estimate the size of the web.
* Differentiate between the concepts of link rot and content drift.

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 04 slides (PDF)](slides-pdf/Module-04-Measure.pdf) | [Module 04 slides (PPTX)](slides-pptx/Module-04-Measure.pptx)

### Discussion Question

Link rot and content drift are important concepts for scholars who use the Web for references. There are three different options for this discussion based on what type of example you might have, or not have:

1. Have you cited links in a paper or report only to later find that they are no longer available or that they no longer contain the information that you wanted to cite? What were the original links?  Was this an issue of link rot or content drift?
1. If you don't have a reference in a paper, do you have an old bookmark that either no longer works or does not contain the information you wanted to bookmark?  Was this a case of link rot or content drift?
1. If you don't have an example of either, then describe the concepts of link rot and content drift and explain how they are different and how each of them could be detrimental to scholarly communication.

For all options, also discuss how the knowledge of link rot and content drift might affect how you will approach using references on the web.

### Summary

Module 4 covered techniques for estimating the size and dynamics of the web. 

# Module 5

## Archiving the Web

**Overview:** This module introduces web archiving. We will start with some motivating examples of why we might want to archive the web. We will also cover how the web is archived and how much of the web is archived. This module also introduces the Memento framework and protocol, which allows for content-negotiation in time. The module ends with examples of user interfaces that allow users to navigate through time on the web.

**Relevance:** The web gives historians and other social scientists significant insight into our society, especially into how technology has affected it. If significant portions of the web are not archived, we might lose a large amount of our digital heritage.

### Objectives

After completing this module, students will be able to

* Explain the importance of web archiving.
* Describe how to find and access archived webpages using the Internet Archive’s Wayback Machine.
* Explain how the Memento Framework allows for content negotiation in the time dimension.
* Differentiate between a URI-R, URI-M, and URI-T in Memento terminology.
* Use the Memgator Memento Aggregator service to download a TimeMap and explain the contents of what is returned.

### Reading Assignment

* M. Weigle, [Importance of Web Archiving](https://items.ssrc.org/parameters/on-the-importance-of-web-archiving/), *SSRC Parameters*, 2018.
* M. Weigle, [Enabling Personal Use of Web Archives](https://www.slideshare.net/mweigle/enabling-personal-use-of-web-archives), slides from keynote talk presented at Web Archiving and Digital Libraries (WADL) 2018

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 05 slides (PDF)](slides-pdf/Module-05-Archive.pdf) | [Module 05 slides (PPTX)](slides-pptx/Module-05-Archive.pptx)

### Discussion Question 

There are two options for discussion:

1. Now that you know more about web archiving, including the Internet Archive, archive.is, Conifer, and other archiving tools, will you change your approach to using online resources in reports? What do you plan to do differently?
1. Discuss an interesting website that you have found archived in the Internet Archive or another web archive. (You can use <https://timetravel.mementoweb.org/> as an aggregator to discover pages in archives other than the Internet Archive.) How well archived was the site? Was enough archived that you were able to use the website as you wanted to?

### Homework Assignment

* [HW2 - Web Archiving](hw/HW2.md)

### Summary

Module 5 introduced web archiving, the Memento protocol for content-negotiation in time, and user interfaces for interacting with web archives. 

# Module 6

## Searching the Web

**Overview:** This module covers the principles of web search. This includes crawling the web, indexing the collected documents, and ranking the results through TF-IDF and link-based metrics like PageRank and HITS.

**Relevance:** Most of us use web search everyday. This module will uncover some of the mechanisms underlying web search.

### Objectives

After completing this module, students will be able to

* Describe the main steps needed for web search.
* Describe what a web crawler does.
* Explain the difference between precision and recall.
* Explain the difference between false positives and false negatives.
* Explain TF-IDF and how it is used to determine relevance in web search.
* Explain the importance of inlinks and outlinks in the Page Rank algorithm.
* Given a query term, compute TF-IDF for the term in a set of documents.

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 06 slides (PDF)](slides-pdf/Module-06-Searching.pdf) | [Module 06 slides (PPTX)](slides-pptx/Module-06-Searching.pptx)

### Homework Assignment

* [HW3 - Ranking Webpages](hw/HW3.md)

### Summary

Module 6 covered web search, including basic concepts of information retrieval such as TF-IDF, precision, and recall, and covered the PageRank model pioneered by Google.  This module completes Unit 1 on Web Science and Web Architecture.

# Unit 2 - Social Networks

Unit 2 consists of 4 modules:

* Module 7: Social Networks
* Module 8: Selection and Social Influence
* Module 9: Visualizing Social Networks
* Module 10: Disinformation

# Module 7

## Social Networks

**Overview:** This module begins our exploration of social networks, both offline and online. We will look at social networks as graphs where nodes are connected by social links. We will also look at the characteristics of these social links, including the properties of strong and weak ties, the triadic closure, tie strength and embeddedness, and how removing highly embedded edges can lead to graph partitioning.

**Relevance:** Social scientists use social networks to study how people interact and develop theories of social behavior. Online social networks (OSNs) offer opportunities to study social networks at a larger scale. Understanding the structure of OSNs can lead to systems in the future that improve security, leverage trust, improve social interaction, etc.

### Objectives

After completing this module, students will be able to

* Describe the friendship paradox.
* Explain the triadic closure in social networks.
* Explain how edge embeddedness affects trust.
* Explain the edge betweenness property.
* Explain the steps in the Girvan-Newman graph partitioning algorithm.

### Reading Assignment

Easley and Kleinberg, [*Networks, Crowds and Markets*](http://www.cs.cornell.edu/home/kleinber/networks-book/) (2010)

* Chapter 2, "Graphs"
* Chapter 3, "Strong and Weak Ties"

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 07 slides (PDF)](slides-pdf/Module-07-Social-Networks.pdf) | [Module 07 slides (PPTX)](slides-pptx/Module-07-Social-Networks.pptx)

### Discussion Question

Have you had the experience of triadic closure in your friend networks?  Does the statement of "triadic closure is more likely to form when initial edges are strong" fit with your experience? Additionally, are you a bridge or local bridge between two friend networks?

### Homework Assignment

* [HW4 - Exploring Social Networks](hw/HW4.md)

### Summary

Module 7 introduced social networks and the concept of analyzing social networks using graphs. Through graphs, we studied the friendship paradox, the triadic closure, edge embeddedness, edge betweenness and the Girvan-Newman graph partitioning algorithm. 

# Module 8

## Selection and Social Influence

**Overview:** This module examines how social networks change over time and the effects of selection and social influence.  We introduce the principle of homophily, which says that we tend to be similar to our friends, and we look at whether homophily in networks is due to selection (we choose friends like ourselves) or social influence (we choose activities or behaviors based on our existing friends). And we examine how to explore these properties in real-world social networks.

**Relevance:** Understanding homophily and the principles of selection and social influence can help us to understand how social networks form and change over time. This, in turn, can help us understand how information spreads through social networks.

### Objectives

After completing this module, students will be able to

* Define homophily.
* Explain how selection affects homophily.
* Explain how social influence affects homophily.
* Explain the difference between focal closure and membership closure in a social-affiliation network.
* Explain the process/steps for measuring how triadic closure is dependent upon the number of shared friends.

### Reading Assignment

* Chapter 4, "Networks in Their Surrounding Contexts" (through Section 4.4) from Easley and Kleinberg, [Networks, Crowds and Markets](http://www.cs.cornell.edu/home/kleinber/networks-book/) (2010)
* [James Fowler on "The Colbert Report"](http://www.cc.com/video-clips/c3suh9/the-colbert-report-james-fowler), January 7, 2010, (4:58)
* Nicholas Christakis, ["The hidden influence of social networks"](https://www.youtube.com/watch?time_continue=1&v=2U-tOghblfE),TED Talk, May 10, 2010, (18:44)

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 08 slides (PDF)](slides-pdf/Module-08-Selection.pdf) | [Module 08 slides (PPTX)](slides-pptx/Module-08-Selection.pptx)

### Discussion Question

Again, think about your relationships.  Which is more common for you?  Have you chosen friends based on common interests or characteristics (selection)?  Have you changed your interests or behaviors because of your existing friends (social influence)?

### Summary 

Module 8 discussed the principle of homophily and how selection and social influence can affect social networks over time. 

# Module 9

## Visualizing Social Networks

**Overview:** This module introduces graph drawing and layout algorithms. We have seen how graphs are used to express social connections, so we will look at graph creation software and how to visualize network graphs in Python and JavaScript, including in D3.js.

**Relevance:** Visualization of social networks is important in understanding how connections form and influence the transfer of information through them.

### Objectives

After completing this module, students will be able to

* List five network data formats.
* Describe a circular graph layout.
* Describe a force-directed graph layout, including the effect of the forces on the edges and nodes.
* Use a Python library to generate a node-link diagram of Zachary’s Karate Club.

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 09 slides (PDF)](slides-pdf/Module-09-Graph-Vis.pdf) | [Module 09 slides (PPTX)](slides-pptx/Module-09-Graph-Vis.pptx)

The slides will reference 

* [NetworkX example Colab notebook](code/NetworkX_example.ipynb)
* [d3 example at Observable](https://observablehq.com/@weiglemc/force-directed-layout-example)

### Homework Assignment

* [HW5 - Graph Partitioning](hw/HW5.md)

### Summary

Module 9 covered the visualization of network graphs. This included network graph formats and software and libraries used to create network graphs from raw data. 

# Module 10

## Disinformation

**Overview:** This module discusses disinformation and how it spreads via social networks and through social media.  A large part of the module features a talk by Dr. Kate Starbird, a professor at the University of Washington and an expert in how information, including disinformation, spreads in social media. The module also covers material from researchers who have studied Russian propaganda and analyzed the characteristics behind this disinformation.

**Relevance:** Becoming aware of disinformation and understanding how it can spread through social networks is an essential part of being an informed citizen in today's environment.

### Objectives

After completing this module, students will be able to

* Explain the difference between disinformation and misinformation.
* Explain how echo chambers and filter bubbles support motivated reasoning and confirmation bias.
* Explain how an understanding of social networks is important in understanding how misinformation and disinformation spreads.
* List the 4 distinctive features of contemporary Russian propaganda.
* List and explain ways to combat the “firehose of falsehood”.

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 10 slides (PDF)](slides-pdf/Module-10-Disinformation.pdf) | [Module 10 slides (PPTX)](slides-pptx/Module-10-Disinformation.pptx)

Watch Kate Starbird, ["Muddied Waters: Online Disinformation During Crisis Events"](https://vimeo.com/266008060), Apr 18, 2018 (52:35)

### Discussion Question

Have you encountered disinformation in your social media feeds?  How did you tell that it was not true?  Did it come from someone that you trusted?  What did you do about it?

### Homework Assignment

* [HW6 - Analyzing Disinformation Domains](hw/HW6.md)

### Summary

Module 10 covered disinformation and how it can spread through social media.  This module concludes Unit 2.

# Unit 3 - Collective Intelligence

Unit 3 consists of 4 modules:

* Module 11: Collective Intelligence and Recommender Systems
* Module 12: Clustering Algorithms
* Module 13: Document Filtering (Classification)
* Module 14: kNN and Algorithm Summary

# Module 11

## Collective Intelligence and Recommender Systems

**Overview:** This module provides an introduction to collective intelligence and recommender systems.  Collective intelligence includes crowdsourcing, human computation, social computing, and data mining. Recommender systems will be studied in the context of recommending movies based on critics' reviews.

**Relevance:** Recommendations are an important part of social media systems. From recommending what accounts to follow to recommending what videos to watch, these systems play a large role in shaping how we interact with social media.

### Objectives

After completing this module, students will be able to

* Describe and define the four components of collective intelligence.
* Explain how collaborative filtering is related to recommender systems.
* Differentiate between Euclidean distance and the Pearson correlation coefficient.
* List three challenges for collaborative filtering.

### Reading Assignment

Toby Segaran, [*Programming Collective Intelligence*](https://www.oreilly.com/library/view/programming-collective-intelligence/9780596529321/) - available [via ODU](https://go.oreilly.com/old-dominion-university/library/view/programming-collective-intelligence/9780596529321/)

* Chapter 1, "Introduction to Collective Intelligence"
* Chapter 2, "Making Recommendations"

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 11 slides (PDF)](slides-pdf/Module-11-CI-Recommender.pdf) | [Module 11 slides (PPTX)](slides-pptx/Module-11-CI-Recommender.pptx)

The slides will reference 

* [PCI Ch2 (Making Recommendations) code examples](PCI_Ch02.ipynb)

### Discussion Question

How have you encountered recommendation systems this week (or month)?  How good were the recommendations?  Was it a collaborative filtering recommendation system or a content-based recommendation system? Was the quality of the recommendation dependent upon how much the system (social network or website) knew about your past behavior and preferences? Are you comfortable with the tradeoff between privacy and improved recommendations?

### Homework Assignment

* [HW7 - Recommender Systems](hw/HW7.md)

### Summary

Module 11 covered collective intelligence, which includes crowdsourcing, human computation, social computing, and data mining.  We covered recommender systems in the context of making movie recommendations. 

# Module 12

## Clustering Algorithms

**Overview:** This module will cover clustering algorithms, used to group similar items without knowing in advance what clusters might be present in the data.  This is an example of unsupervised learning.  We will cover hierarchical clustering and the dendrogram (for visualizing the hierarchy), k-means clustering, and multidimensional scaling (MDS) for visualizing the results of clustering in multiple dimensions.

**Relevance:** Clustering algorithms are used in a variety of applications, especially those where we want to find unknown groups or patterns in our data.  Clustering is an important example of unsupervised learning.

### Objectives

After completing this module, students will be able to

* Distinguish between unsupervised learning and supervised learning.
* Differentiate between agglomerative and divisive clustering.
* Explain how a dendrogram is constructed.
* Explain the main steps in k-means clustering.
* Describe the purpose of multidimensional scaling (MDS).
* Explain the steps of multidimensional scaling.

### Reading Assignment

Toby Segaran, [*Programming Collective Intelligence*](https://www.oreilly.com/library/view/programming-collective-intelligence/9780596529321/) - available [via ODU](https://go.oreilly.com/old-dominion-university/library/view/programming-collective-intelligence/9780596529321/)

* Chapter 3, "Discovering Groups"

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 12 slides (PDF)](slides-pdf/Module-12-Clustering.pdf) | [Module 12 slides (PPTX)](slides-pptx/Module-12-Clustering.pptx)

The slides will reference 

* 365 Data Science video, ["Flat and Hierarchical Clustering | The Dendrogram Explained"](https://www.youtube.com/watch?v=ijUMKMC4f9I) (8:26)
* 365 Data Science video, ["K Means Clustering: Pros and Cons of K Means Clustering"](https://www.youtube.com/watch?v=YIGtalP1mv0) - watch up to time 4:44
* [PCI Ch3 (Discovering Groups) code examples](PCI_Ch03.ipynb)

### Homework Assignment

* [HW8 - Clustering](hw/HW8.md)

### Summary

In Module 12, we discussed clustering algorithms, including hierarchical clustering, k-means clustering, and multidimensional scaling, used to visualize clustering done in multiple dimensions.  We looked at clustering algorithms with the application of grouping similar blogs together based on the words used in the blogs. 

# Module 13 

## Document Filtering (Classification)

**Overview:**  In this module, we will cover classification in the context of document filtering, which is an example of supervised learning.  We will cover the basic probability theory behind classification and study a Bayesian classifier. The driving example used in this module is to classify email as spam or not spam.

**Relevance:** Being able to develop and train automated classification tools is important to allow humans to be able to make sense of the massive amounts of data being gathered today. This includes identifying spam email, but can also be applied to many other types of problems.

### Objectives

After completing this module, students will be able to

* Differentiate between clustering and classification.
* Explain the general steps in classification.
* Explain the purpose of training sets and testing sets in supervised learning.
* Explain how Bayes’ Rule is used in a Naive Bayes Classifier.
* Train and test a Naive Bayes Classifier and draw a confusion matrix for the classification results.

### Reading Assignment

* Toby Segaran, [*Programming Collective Intelligence*](https://www.oreilly.com/library/view/programming-collective-intelligence/9780596529321/) - available [via ODU](https://go.oreilly.com/old-dominion-university/library/view/programming-collective-intelligence/9780596529321/)
    * Chapter 6, "Document Filtering"
* Chapter 9, "Classification and Clustering" (just until Section 9.1.2) from [*Search Engines: Information Retrieval in Practice*](https://ciir.cs.umass.edu/irbook/) by Croft, Metzler, and Strohman

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 13 slides (PDF)](slides-pdf/Module-13-Document-Filtering.pdf) | [Module 13 slides (PPTX)](slides-pptx/Module-13-Document-Filtering.pptx)

The slides will reference 

* [PCI Ch6 (Document Filtering) code examples](PCI_Ch06.ipynb)

### Discussion Question

This week, we've explored simple methods for detecting spam email.  How well do your spam email filters work?  What are common characteristics that you've seen in spam emails?  What are some other techniques for detecting spam emails that could improve upon the simple methods we've discussed?

### Homework Assignment

* [HW9 - Email Classification](hw/HW9.md)

### Summary

Module 13 introduced classification, an example of supervised learning. We covered the probability theory behind Bayesian classifiers and demonstrated how it could be used to train and test a classifier to detect spam email. 

# Module 14 

## kNN and Algorithm Summary

**Overview:** Our final module will cover the k Nearest Neighbors (kNN) prediction model including methods for validating and optimizing the kNN model, and provide an overview of the algorithms covered in this unit. The driving example in this module will be using kNN to predict wine prices.

**Relevance:** kNN prediction has been used in a wide range of applications, including building price models that can help to determine the real value of an item.

### Objectives

After completing this module, students will be able to

* Describe the main idea behind the k-nearest neighbor algorithm.
* Describe the tradeoffs in setting the value of k (not too low, not too high).
* Explain the benefits of weighted kNN.
* Explain the purpose of cross-validation in evaluating prediction algorithms.
* Explain the purpose of the cost function in optimization.

### Reading Assignment

Toby Segaran, [*Programming Collective Intelligence*](https://www.oreilly.com/library/view/programming-collective-intelligence/9780596529321/) - available [via ODU](https://go.oreilly.com/old-dominion-university/library/view/programming-collective-intelligence/9780596529321/)

* Chapter 8, "Building Price Models", code available at [Ch8 GitHub repo](https://github.com/arthur-e/Programming-Collective-Intelligence/tree/master/chapter8)
* Chapter 12, "Algorithm Summary"

### Materials

Each set of lecture slides is available in PDF and PowerPoint (PPTX) formats.

[Module 14 slides (PDF)](slides-pdf/Module-14-kNN-Summary.pdf) | [Module 14 slides (PPTX)](slides-pptx/Module-14-kNN-Summary.pptx)

The slides will reference 

* [PCI Ch8 (Building Price Models) code examples](PCI_Ch08.ipynb)

### Summary

Module 14 covered the kNN prediction algorithm and provided an overview of the algorithms covered in this unit. This provided you with a brief introduction to machine learning algorithms, including both unsupervised methods, like hierarchical and k-means clustering, and supervised methods, like Bayesian classifiers.
