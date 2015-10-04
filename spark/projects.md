### List of End to End projects in spark

#### Word Count and Log processing examples in slides

These examples are present in the **Intro to Spark** slides that I prepared. In order to showcase hello world programs to students, these two examples can serve as perfect initial assignments for the course. Data set will be easily available for both the examples.

#### More practice on RDDs, actions and transformation (For Lab assignment):
- Trying out different ways to create RDD : from texfile, from Python list, from Cassandra , from HDFS.
- Tring out diffferent transformations: map, filter, flatMap, distinct, groupByKey, reduceByKey.
- Trying out different actions: collect, take, first, count, reduce.

#### Extending the log procesing example to have few integrations with other systems:
- Storing cleaned data in some data store like Cassandra, s3, . This will involve the example of how to communicate with cassandra or other data sources.
- Querying the data using sparkSQL or cassandra queries.

The above two projects can act as starting point for students to get their hands dirty with spark functionalities. Infact, they are very neccessary to understand the workflow of RDD, traformations and actions. 

#### Music/Movie recomendation Engine
- This is an example from book "Advanced Analytics with Spark - Sandy Ryza, Uri Laserson, Sean Owen, and Josh Wills" . Its chapter 3 in the book.
##### Data Set:
- Data set is readily available for both [Movie](http://grouplens.org/datasets/movielens/) and [Music](https://www.kaggle.com/c/msdchallenge/data).
##### Algorithmic Perspective:
- Involves understanding of collaborative recomendation algorithms (The book uses Alternating Least Squares Recommender Algorithm)

##### Example implementaions:
- Can be implemented from end to end using Python.
- [Movie recomendation example](http://www.slideshare.net/CasertaConcepts/analytics-week-recommendations-on-spark)

#### A toy example of Lambda architecture for real-time analysis of hashtags in twitter. 
- https://github.com/pereferrera/trident-lambda-splout
- This example can be converted to work with spark. As spark has both offline and online processing capabilitites, this can be very good example for a project.
- Data set can be easily available from twitter API.
- Can be implemented from end to end using Python.

#### Social network analysis by lambda architecture:
- http://www.drdobbs.com/database/applying-the-big-data-lambda-architectur/240162604
- This is interesting project. But somewhat difficult to obtain data set.
- User tries to find relation between users by mining their different social profiles: facebook, twitter, linkedIn, google+.  "I want to be able to capture whether I happen to know someone from multiple social networks, such as Twitter or LinkedIn, or from real-life circumstances" - [webpage](http://www.drdobbs.com/database/applying-the-big-data-lambda-architectur/240162604)

#### Crime Data Classification using Spark MLlib #####
##### Learning Objectives : 
- Feature Engineering
- Applying Deep Learning packages to build classification models
- Multiple models can be compared using various model evaluation strategies  
 
##### Details
- This is an open online competition on [Kaggle.com](https://www.kaggle.com/c/sf-crime/data)
- Using Spark ML library [Spark MLLib](https://spark.apache.org/docs/1.1.0/mllib-guide.html) packages, state of the art classification algorithms such as Decision Tree, SVM, naive Bayes, logistic regression can be applied. 
- Basic Exploratory Data Analysis can be performed using pyspark packages



#### Twitter Streaming Language Classifier.
- https://databricks.gitbooks.io/databricks-spark-reference-applications/content/twitter_classifier/index.html
- This simple example will provide a hands-on experience with Spark Streaming, Spark SQL and Spark MLLib.
- It is divided into three parts:
  Part 1: Fetching twitter tweets in real time using Spark Streaming twitter library and storing them in files. 
  Part 2: Perform some exploratory analysis on the data collected using Spark SQL, for example: count the total number of tweets for the most common languages. The idea is to understand the distribution of tweets across languages. Now, train a model using one of the Spark MLLib algorithms such as KMeans to classify these tweets into different clusters of languages. The number of clusters and number of iterations can be configured.
  Part 3: Once the model is trained, use Spark streaming libraries to fetch live tweets. Apply the model on the tweets, filtering out only those which match a specified cluster and printing those matching tweets.


#### Real-Time Stream Processing and Elasticsearch:
- https://github.com/skrusche63/spark-elastic
- In this project, we can use Spark Streaming as a consumer and aggregator of tracking data streams, and perform a live indexing using elastic search.
- Various real time analytics applications can be build using this combination using financial, adtech, user behavior, Internet of things data, etc.

#### Understanding Wikipedia with Latent Semantic Analysis:
- Wikipedia Dataset is easily available [webpage](https://en.wikipedia.org/wiki/Wikipedia:Database_download)
- This is a basic text analysis project. Pipeline starts with converting xml files to text files followed by stopwords filetring, lemmatizations, computing TF-IDF scores and building term-document matrix. 
- Next we apply dimensionality reduction techniques such as SVD, PCA (Spark's MLlib library)
- Finally, we can apply latent semantic analysis techniques to find Term-Term relevance, Term-Document relevance, Document-Document relevance, etc.
