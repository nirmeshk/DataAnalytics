### List of End to End projects in spark

#### Word Count and Log processing examples in slides

These examples are present in the Intro to spark slides that I prepared. In order to showcase hello world programs to students, these two examples can serve as perfect initial assignments for the course. Data set will be easily available for both the examples.

#### Extending the log procesing to an end to end data processing pipeline in spark that involves:
- Storing cleaned data in some data store like Cassandra, s3, . This will involve the example of how to communicate with cassandra or other data sources.
- Querying the data using sparkSQL or cassandra queries.

The above two projects can act as starting point for students to get their hands dirty with spark functionalities. 

#### Music recomendation Engine
- This is an example from book "Advanced Analytics with Spark - Sandy Ryza, Uri Laserson, Sean Owen, and Josh Wills" . Its chapter 3 in the book.
- Data set is readily available.
- Involves understanding of collaborative recomendation algorithms (The book uses Alternating Least Squares Recommender Algorithm)
- Can be used for movie recomendation as well. Data set is available at http://grouplens.org/datasets/movielens/
- Can be implemented from end to end using Python.

#### A toy example of Lambda architecture for real-time analysis of hashtags in twitter. 
- https://github.com/pereferrera/trident-lambda-splout
- This example can be converted to work with spark. As spark has both offline and online processing capabilitites, this can be very good example for a project.
- Data set can be easily available from twitter API.
- Can be implemented from end to end using Python.

#### Social network analysis by lambda architecture:
- This is interesting project. But somewhat difficult to obtain data set.
- User tries to find relation between users by mining their different social profiles: facebook, twitter, linkedIn, google+.  "I want to be able to capture whether I happen to know someone from multiple social networks, such as Twitter or LinkedIn, or from real-life circumstances" - [webpage](http://www.drdobbs.com/database/applying-the-big-data-lambda-architectur/240162604)
