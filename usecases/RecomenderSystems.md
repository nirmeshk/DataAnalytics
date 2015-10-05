## Music/Movie recomendation Engine

### Overview
The goal of recomendation sysem is to predict the preference of user. For e.g, which movies the user will like, which products user will buy on amazon based on his/her past history.

### Data Set and Sample Code repositories
- Music recomendation example from book "Advanced Analytics with Spark - Sandy Ryza, Uri Laserson, Sean Owen, and Josh Wills" . Data set is readily available at [link](http://www-etud.iro.umontreal.ca/~bergstrj/audioscrobbler_data.html). The example uses Collaborative technique for recomending the songs that user may like.
- The Million Song Dataset Challenge [paper](https://www.ee.columbia.edu/~dpwe/pubs/McFeeBEL12-MSDC.pdf) and [Kaggle competition](https://www.kaggle.com/c/msdchallenge).
- Movielens data set by University of Minnesota (http://grouplens.org/datasets/movielens/) and their recomendation engine in Java [lenskit] (https://github.com/lenskit/lenskit)

### Literature available:
- Collaborative Filtering for Implicit Feedback Datasets - Yifan Hu, Yehuda Koren, Chris Volinsky [link](http://yifanhu.net/PUB/cf.pdf)
- Deep content-based music recommendation - Aaron van den Oord, Sander Dieleman, Benjamin Schrauwen [link](http://papers.nips.cc/paper/5004-deep-content-based-music-recommendation.pdf)
- The Million Song Dataset Challenge [link](https://www.ee.columbia.edu/~dpwe/pubs/McFeeBEL12-MSDC.pdf)
- A survey paper on recomendations using movie lens data set: Collaborative Filtering Recommender Systems By Michael D. Ekstrand, John T. Riedl and Joseph A. Konstan [link](http://files.grouplens.org/papers/FnT%20CF%20Recsys%20Survey.pdf) 


### Famous Algorithms used:
- Collaborative filtering based on matrix factorization.
- Content based filtering using meta data of songs/movies. This may involve numbe of machine learning techniques - both classification and regression.
