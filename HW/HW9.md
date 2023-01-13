# Homework 9 - Email Classification
**Due:** In 2 weeks

## Assignment

The goal of this assignment is to classify email into two groups based on topic -- either "on topic" or "not on topic".  You can choose the topic based on what types of emails you typically receive (or what you have access to).

Write a report that answers and *explains how you arrived at the answers* to the following questions.  

**Tips for Completing this Assignment:**
* First, read the entire assignment before starting.
* *Don't start with a Google search.*  Your first references should be
    * Module 13 slides
    * [class Colab notebook](432_PCI_Ch06.ipynb)
    * [*Programming Collective Intelligence* book](https://go.oreilly.com/old-dominion-university/library/view/programming-collective-intelligence/9780596529321/) and [Chapter 6 code](https://github.com/arthur-e/Programming-Collective-Intelligence/tree/master/chapter6)  

### Q1. Create two datasets, Testing and Training.

You may choose a topic to classify your emails on (but choose only 1 topic). This can be spam, shopping emails, school emails, etc. 

The **Training** dataset should consist of
* 20 text documents for email messages you consider on your chosen topic
* 20 text documents for email messages you consider *not* on your chosen topic

The **Testing** dataset should consist of:
* 5 text documents for email messages you consider on your chosen topic
* 5 text documents for email messages you consider *not* on your chosen topic

Make sure that these are plain-text documents and that they do not include HTML tags.  The documents in the Testing set should be different than the documents in the Training set.

Upload your datasets to your GitHub repo. *Please do not include emails that contain sensitive information.*

*Q: What topic did you decide to classify on?*

### Q2. Naive Bayes classifier
Use the example code in the class Colab notebook to train and test the Naive Bayes classifier.  
* Use your *Training* dataset to *train* the Naive Bayes classifier.  
* Use your *Testing* dataset to *test* the Naive Bayes classifier.

Create a table to report the classification results for each email message in the *Testing* dataset.  The table should include what the classifier reported (on-topic or off-topic) and the actual classification.

*Q: For those emails that the classifier got wrong, what factors might have caused the classifier to be incorrect?  You will need to look at the text of the email to determine this.*

### Q3. Confusion Matrix
Draw a confusion matrix for your classification results (see Module 13, slides 40, 42, 43).  

*Q: Based on the results in the confusion matrix, how well did the classifier perform?*  

*Q: Would you prefer an email classifier to have more false positives or more false negatives?  Why?*

## Extra Credit

### Q4 

Report the precision and accuracy scores of your classification results (see Module 13, slide 43).  Include the formulas you used to compute these values.

### Q5 

Tune your classifier by updating weights to obtain better classification results. You may want to change the default weights (`weight`, `ap`) given to `weightedprob()` or the threshold used for the Bayesian classifier or change how the words are extracted from the document (for this you will need to re-train the model).  Report the changes you made, re-run your Testing dataset, and show that the performance improved (either by using the confusion matrix or by computing precision and accuracy).

If your classifier got all of the items correct in Q2, change the weights to make the classifier perform worse and discuss the results.

### Q6 

Implement the classifier with the Multinomial model instead of the multiple Bernoulli model and re-run Q2 and Q3.  Did the classification improve?  *Make sure to remove the unique word filter from the extractor.*
