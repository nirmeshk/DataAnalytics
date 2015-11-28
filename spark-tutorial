Spark Tutorial
==================
### Submision Instructions:
- For successfull completion of this tutorial, you will need to submit the log of the commands that you ran on spark interactive shell. Instructions on how to unable logging is given in 'Enable REPL to store history' section.
- You are free to try extra commands of your choice.

### System Requirements:
------------------------
- For the purpose of this tutorial and rest of projects in Spark, we will be using `Ubuntu 14.04 64-bit` as our operating system of choice.
- If you have OS-X, you should be fine. No need for virtual machines.
- If you have windows, boot an ubuntu instance inside virtual box or use one of the configured VCL box for the course.

- Once you have OS ready, make sure you have following requirements installed for smooth operations:
  + Java installed on the machine. Infomation on installing JAVA on ubuntu can be found [link](https://www.digitalocean.com/community/tutorials/how-to-install-java-on-ubuntu-with-apt-get). To making sure java is correctly installed, use following command: `java -version       #should print the current`
  + Python 2.7.x (This comes pre-installed with Ubuntu).
  + Pip installer for python `sudo apt-get install python-pip`
  + Python developer dependencies `sudo apt-get install python-dev`
  + Ipython `sudo pip install ipython`

### Installation
----------------
- Download the latest spark from http://spark.apache.org/downloads.html . In the form, choose latest version of spark. In package type, select "Prebuilt for Hadoop 2.x and later".

```bash
# Download spark 1.5 pre built with hadoop 2.6
curl -O http://apache.arvixe.com/spark/spark-1.5.2/spark-1.5.2-bin-hadoop2.6.tgz
tar -xvf spark-1.5.2-bin-hadoop2.6.tgz   # extract the compressed file
cd spark-1.5.2-bin-hadoop2.6     # change directory into spark

# Run Hello world example to calculate value of Pi.
./bin/run-example SparkPi 10
```
- If everything is correct, your spark engine should start and shut down for a second.

- Set the $SPARK_HOME environment variable for all the future references. 
- Add following to you `$HOME/.bashrc`:

`export SPARK_HOME="$HOME/spark-1.5.0-bin-hadoop2.6/"`
- Don't forget to `source $HOME/.bashrc`

### REPL s are Awesome
----------------------
- The best way to get one's feet wet with Spark, is to use its in build REPL to try things out.
- REPL stands for read–eval–print loop, a.k.a interactive shell for language. Many modern languages(Python, Scala, Ruby) provide the REPL functionality. E.g for python, you can `$ python` on terminal to start interactive shell where you can try the python commands.
- Spark provides REPL for scala and python. We an start python REPL by typing `$SPARK_HOME/bin/pyspark`
- Type some commands of python as well as spark to get a feel
```python
print(sc)
print("Hello world")
a = sc.parallelize([1, 2, 3, 4])
a.collect()
```
- `sc` stands for spark context. A SparkContext represents the connection to a Spark cluster, and can be used to create RDDs, accumulators and broadcast variables on that cluster. For now, we can just treat it as a requirement that is already satisfied within SPARK REPL. If you creating a standalone program, you will need to define te SPARK Context.

#### Enable REPL to store history
- In order to make submission for this assignment, you will submit the history of the commands that you ran on interactive Shell.

- In order to save the history, we will connect `ipython` with spark shell.

- Make sure you have ipython installed `ipython --version`

- Start the shell by typing `IPYTHON=1 $SPARK_HOME/bin/pyspark`

- To save history, run `%logstart <history_file> append` where `<history_file>` is the name of the file that you want to store history to. Once you are finish with the `%logstop` to stop logging.

### Introduction To Spark
-----------------------------
- To know what Spark is, read chapter-1 from the book Learning Spark : Lightning-fast Data Analytics By Karau, Holden, Zaharia, Matei, Wendell, Patrick, Konwinski, Andy. The book is available online on ncsu library (http://catalog.lib.ncsu.edu/record/NCSU3500562)
- Chapter 1 of the book is also available in free sampler (http://cdn.oreillystatic.com/oreilly/booksamplers/9781449358624_sampler.pdf)
- **Note:** It is highly recomended **to not** move forward before reading this intro.

### The mighty RDD's
-----------------------------
- An RDD is simply a distributed collection of elements.
- InSpark **all work** is expressed as either creating new RDDs, transforming existingRDDs, or calling operations on RDDs to compute a result.
- Under the hood, Spark automatically distributes the data contained in RDDs across your cluster and parallel‐izes the operations you perform on them.
- **Tip For starters:**  you can treate RDD as simple collection found in the languages(Example: python list or Java ArrayList). This way you can do all the magic by not worrying about how the data is distributed across the cluster. For you, its single list that can be operated upon.
- Somewhere down the line, you will need to understand the concept in depth, but for now, do not sweat much.

```python
# Create RDD from python list
rdd_1 = sc.parallelize([1, 2, 3, 4, 5, 6, 7])
# So basically, we wrapped our python list into some abstraction.
# If this list was say 1 billion numbers, spark would have partitioned the data under the hood.
# But for you, the programming will be convenient as it is just a collection.

# Create RDD from text file
# Each line will be treated as one entry in RD
my_rdd_2 = sc.textFile('data/mllib/pic_data.txt')
```

### Actions and Transformations:
--------------------------------
- We can perform Actions and/or Transformations on RDD.

#### Actions

- Actions give you results.
- The result can be returned to driver program for printing or other use as shown above, or may be stored to some external storage.

1. *collect()*
  - Return a list that contains all of the elements in this RDD.
  ```python
  rdd_1 = sc.parallelize([1, 2, 3])
  rdd_1.collect() 
  ```
2. *count(), first(), take()*
  - Return the number of elements in this RDD
  ```python
  c = rdd_1.count()               # Return number of entries in RDD
  print(c)
  rdd_1.first()                   # Return first element of RDD
  rdd_1.take(5)                   # Return first 5 elemnts and return them as python list
  ```
3. *saveAsTextFile()*
  ```python
  rdd_1.saveAsTextFile('tmp.txt') # Save the RDD to text file.
  ```

4. *reduce()*
  - Reduces the elements of this RDD using the specified commutative and associative binary operator
  ```python
  def add(x, y):
    return x + y
  
  def multiply(x, y):
    return x * y
  
  
  rdd_1 = sc.parallelize([1, 2, 3, 4])
  rdd_1.reduce(add)
  # output: 10
  rdd_1.reduce(multiply)
  # output: 24
  ```

#### Transformations

- Transformation are operations on RDD that creates a new RDD.
- In other words, we *"Trasform"* one rdd to another.
- Example of transformations:
  + Square all the entries in rdd.
  + Remove all the negative entries or null values from rdd.
  + Split each line in rdd to create list of words.
  + Filter all the error lines from log files.

1. *map()* 
  - The most frequent transformation you will be doing in "map". 
  - rdd.map(func) : apply *func* to each element of rdd.
  ```python
  def square(x): 
    return x**2
  
  rdd_squared = rdd_1.map(square)   # Create a new RDD with the squares of rdd_1
  rdd_squared.collect()             # Print the list
  
  # For such small functions, we can use lambda expressions. 
  # Just for refresher, lambda is a shorthand notation for creating small functions on fly. 
  # The syntax is::  lambda <parameter>: <expresion>
  
  rdd_squared = rdd_1.map(lambda x: x**2)
  ```
2. *filter()*
  - Create a new rdd by filtering out the entries depending on certain conditions.
  ```python
  def positive(x):
    if x> 0: 
      return True
    else:
      return False
  
  rdd_1 = sc.parallelize([1, 2, -3, 4, -5, 6, 7])
  rdd_pos = rdd_1.filter(positive)
  rdd_pos.collect()
  
  # Let us try to use lambda again for shortening the expression:
  rdd_1.filter(lambda x: x > 0).collect() # Also, Combined transformation and action into one
  ```
3. *groupByKey()*
  - Return an RDD of grouped items. 
  ```python
  rdd = sc.parallelize([("a", 1), ("a", 2), ("b", 1) ])
  rdd_grouped = rdd.groupByKey()
  rdd_grouped.collect()
  # Output: [('a', [1, 2]), ('b', [1])]
  ```
4. *flatMap()*
  - Return a new RDD by first applying a function to all elements of this RDD, and then flattening the results.
  ```python
  rdd = sc.parallelize([2, 3, 4])
  
  # Let us first use map
  rdd.map(lambda x: range(1,x)).collect()
  # output: [[1], [1, 2], [1, 2, 3]]
  
  # Applying same function with flatMap
  rdd.flatMap(lambda x: range(1,x)).collect()
  # output: [1, 1, 2, 1, 2, 3]  # Note how flat map "flattened" the nested lists
  ```

### Putting it all together.. finally a word count
---------------------------------------------------

```python
text = sc.parallelize(["I stepped on a Corn Flake, now I am a Cereal Killer", \
              "Hello world inside hello world", "Banana error", \
              "Not Lorem Ipsum", "what a wonderfull day", "what up?"])
counts = text.flatMap(lambda line: line.split(" ")) \
             .map(lambda word: (word, 1)) \
             .reduceByKey(lambda a, b: a + b)
counts.collect()
```

### More example.. Log processing
----------------------------------
Create a log.log file inside $SPARK_HOME/ with following content
```
[INFO] Some random info about mysql 
[ERROR] Some random about Mysql
[INFO] Some random info about mysql 
[INFO] Some random info about mysql 
[ERROR] Some random about Java
[ERROR] Some random about Mysql
[ERROR] Some random about Mysql
[INFO] Some random info about java 
[ERROR] Some random about Java
[ERROR] Some random about Mysql
```

Task: 
  - calculate total number of errors in log file
  - calculate number of mysql and java error counts individually

```python 
rdd = sc.textFile('log.log')

# count number of errors
rdd_error = rdd.filter(lambda line: 'ERROR' in line)
rdd_error.count()

# count mysql errors
rdd_error.filter(lambda line: 'Mysql' in line).count()

# count java errors
rdd_error.filter(lambda line: 'Java' in line).count()
```

###  Once you are finished, run `%logstop` and submit the log file.  

### References:
- http://spark.apache.org/docs/latest/api/python/pyspark.html#pyspark.RDD
- http://spark.apache.org/examples.html
- Learning Spark : Lightning-fast Data Analytics By Karau, Holden, Zaharia, Matei, Wendell, Patrick, Konwinski, Andy




