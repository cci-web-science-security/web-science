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

### Homework Assignment

Explore some of the tools that will be used during the course:

* [Twitter, twarc](getting-started/twitter-setup.md) - follow the instructions to set up your access to the Twitter API and isntall the twarc tool
* [Working with tweets](getting-started/working-with-tweets.md) - use the provided Python scripts to collect and process a small set of tweets
* [Memgator](getting-started/memgator.md) - follow the instructions to set up and test a local instance of the Memgator tool

### Summary

Module 1 introduced the field of web science as an interdisciplinary study of the Web's properties, protocols, algorithms, and societal effects. You completed learning checks reviewing basic material, completed a homework assignment that introduced the software and tools we will use this semester, and participated in a class discussion with students introducing themselves to their classmates.

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

Module 2 introduced Python, the main programming language used for homework assignments this semester. We covered basic syntax and the use of libraries such as requests and Beautiful Soup. You completed learning checks reviewing basic material, experimented with Python code examples, and participated in a class discussion where you provided examples of how you have encountered web science in your daily life over the past month.
