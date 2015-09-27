## Spark

System: Ubuntu 14.04 64-bit

- Make sure you have Java installed on the machine. Infomation on installing JAVA on ubuntu can be found [link](https://www.digitalocean.com/community/tutorials/how-to-install-java-on-ubuntu-with-apt-get). For making sure java is correctly installed, use following two commands:
  ```bash
  java -version       #should print the current java version
  ```

- Spark is distributed data processing engine. In order to store data, it requires one of the distributed filesystems. One of the prefered choice is HDFS (Hadoop file system). To install spark on Ubuntu, we will be using the distribution that already has Hadoop built-in.
- Download the latest spark from http://spark.apache.org/downloads.html . In the form, choose latest version of spark. In package type, select "Prebuilt for Hadoop 2.x and later". 

```bash
# Download spark 1.5 pre built with hadoop 2.6
curl -O http://apache.arvixe.com/spark/spark-1.5.0/spark-1.5.0-bin-hadoop2.6.tgz 
tar -xvf spark-1.5.0-bin-hadoop2.6.tgz   # extract the compressed file
cd spark-1.5.0-bin-hadoop2.6     # change directory into spark

# Run Hello world example to calculate value of Pi.
./bin/run-example SparkPi 10
```
- If everything is correct, your spark engine should start and shut down for a second.
