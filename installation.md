## Spark Installation on Ubuntu

1. Make sure you have Java installed on the machine, and JAVA_HOME added to your PATH. Infomation on installing JAVA on ubuntu can be found [link](https://www.digitalocean.com/community/tutorials/how-to-install-java-on-ubuntu-with-apt-get). **Note:** Don't forget to set JAVA_HOME enviornment variable. 
2. Spark is distributed data processing engine. In order to store data, it requires one of the distributed filesystems. One of the prefered choice is HDFS (Hadoop file system). To install spark on Ubuntu, we will be using the distribution that already has Hadoop built-in.
  - Download the latest spark from http://spark.apache.org/downloads.html . In the form, choose latest version of spark. In package type, select "Prebuilt for Hadoop 2.x and later". 
  - I downloaded the spark-1.4.1 library by `wget http://apache.arvixe.com//spark/spark-1.4.1/spark-1.4.1-bin-hadoop2.6.tgz` Note: this link might not work in future.
3. Unzip the contents of the file using `tar -xvf spark-1.4.1-bin-hadoop2.6.tgz`.
4. Change directory to the unziped content. `cd spark-1.4.1-bin-hadoop2.6/` 
5. Run `./bin/run-example SparkPi 10`. If everything is correct, your spark engine should start and shut down for a second.

## STINGER (georgiatech) Installation

Stinger has detailed installation instructions given on http://www.stingergraph.com/index.php?id=getting-started
