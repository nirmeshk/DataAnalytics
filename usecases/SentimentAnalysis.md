# Sentiment Analysis

Sentiment Analysis can be used to automatically detects emotions, speculations, evaluations and opinions in the content that people write.

# Usescase:
## Movie sentiment based on movie reviews written by users:
### Data : 
1. Data consists ofa set of 25,000 highly polar movie reviews for training, and 25,000 for testing. There is additional unlabeled data for use as well. Raw text and already processed bag of words formats are provided. See the README file contained in the release for more details. [IMDB Data](https://www.dropbox.com/s/zm8fgjmpcu7080b/aclImdb_v1.tar.gz?dl=0)
2. Movie Review Dataset Provided by Cornell : http://www.cs.cornell.edu/people/pabo/movie-review-data/

### Packages and Implementations:
1. Python [NLTK](http://text-processing.com/demo/sentiment/) Movie review API and demo
2. Python [LDA](http://chrisstrelioff.ws/sandbox/2014/11/13/getting_started_with_latent_dirichlet_allocation_in_python.html) Python package for LDA
3. Stanford Implementation and Paper on [RNN] (http://nlp.stanford.edu/sentiment/)
4. Sentiment Analysis with Spark [Sample Project](https://github.com/zdata-inc/SparkSampleProject)
5. [Spark MLlib for LDA] (http://spark.apache.org/docs/latest/mllib-clustering.html#latent-dirichlet-allocation-lda)

### Algorithms:
1. Latent Dirichlet Allocation(LDA)
  - Publication : Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, and Christopher Potts. (2011). [Learning Word Vectors for Sentiment Analysis](http://ai.stanford.edu/~amaas/papers/wvSent_acl2011.pdf)

2. Recursive and Recurrent Neural Network (RNN)
  - Publications: [Sentiment Analysis on Movie Reviews using Recursive and Recurrent Neural Network Architectures](https://cs224d.stanford.edu/reports/TimmarajuAditya.pdf)
