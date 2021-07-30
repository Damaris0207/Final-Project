# Book Recommender Prototype 📚🔍
by Dàmaris Clariana, July 2021

## Index

- [Introduction](#introduction)
- [Finding and processing the data](#finding-and-processing-the-data)
- [Visualisations](#visualisations)
- [Limitations and projection](#limitations-and-projection)
- [Refferences](#refferences)


## Introduction

__Scenario__: Being a reader all these years and working in my firsts jobs in bookshops, i've realized that there is no such thing as a book recommender. There are several websites and book apps, but they are or kind of social media (making community, connecting, sharing about books...) or kind of reading support (where you can register your process with the book, how you feeling...) but this is not a recommender in itself.

__Challenge1__: Own data collection! I couldn't find an interesting dataset with data beyond isbn, author and genre. So I went through collecting data directly from people. I created a survey which you can find [here](https://forms.gle/z6HBgGfnrAy81Dtn9). 

__Challenge2__: Processing a lot of text data for shaping a recommender code.

__Results__: Got a first prototype of a book recommender based on the books collected in the survey. You can find the recommender at the bottom of the jupyter notebook from this repository. Also you can see our [class presentation](https://drive.google.com/file/d/1JxLL0juF8P0MnpJ2_gK-u50TGUQVsIao/view?usp=sharing).

--> You can follow the evolution of the project on my [trello board](https://trello.com/b/fhAYHpFb/book-recommender).




## Finding and processing the data 


__Challenges and modeling unsupervised machine learning__:
- Got the data from the survey, that easily transformed into an excel readable in python. 
- The data was pretty clean but in a hard level of complexity in order fit into an algorithm model.
- Needed to transform some columns with OneHotEncoder.
- Chose an unsupervised machine learning model: KMEANS - CLUSTER
- Approached clusters model because I was looking for grouping books by similarities between them. So that when a user enters his preferences for a book, the algorithm search the best cluster that is closer to his interests.
- Got 12 clusters created and aggregated to the dataset.
- Built a python code for the recommender joining all the processes done before. 


__Learnings__: How to work with OneHotEncoder and KMEANS model. Also, the recommender has to include 3 parts: 
1. Where you store the user preferences.
2. Where you transform them into a dataframe(table) comparable to the processed dataset.
3. Where you bring the keys for the model in order to predict the best cluster for the user.  




## Visualisations

Here is the link to the project's [visualisations](https://public.tableau.com/app/profile/d.maris.clariana/viz/Bookrecommendervisuals/Proportionsforgenres?publish=yes).
You can find some descriptive statistics from my survey sample like these:
- Proportions of books by genre
- Character gender by genre AND cluster
- Original languages
- Groups of books by publication dates
- Word frequency analysis by genre


## Limitations and projection

OWN DATA COLLECTION
As I already said, this data collection looks an easy thing but the data is really reach and complex. There is a lot of information you can extract from it. 
But you need to previously know which is the best way to do it. 

COMPLEXITY
For that reason, I could only work with a half of the columns of the dataset, the ones more straight forward and the ones that were feasible to transform in a little time.

SHORT TIME
The short time couldn't allow me to get more further and to study other techniques that my project maybe required.

TEXT ANALYSIS
At the starting point of the project, I wanted to take advantage of the heavy text columns and do Sentiment Analysis to get a score number and add it to the Machine Learning model, but the difficulties with the translation API and the short time were the biggest impediments.

So I could only do text analysis and, for example, look for most popular words and quotes lengths. But it's okay, it's a first prototype built in 5 days.



FUTURE PROJECTION
For the future I would like to be able to improve this project and extract all the information the data contains. And also keep surveying and keep collecting more data in an improved way.




Thanks for reading!

## Refferences

Other references and sources I consulted about literary concepts! These helped me to shape the survey:

https://literaryterms.net/
https://www.oprahdaily.com/entertainment/books/a29576863/types-of-book-genres/
https://self-publishingschool.com/book-genres/
https://www.homohominisacrares.net/artes-literatura/generos-de-novelas.php
