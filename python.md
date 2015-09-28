## Work In Progress !!

### Getting upto the speed with basic Python syntax
- [Google's Python tutorial for programmers](https://developers.google.com/edu/python/)

### Some concepts that you will need for understanding Spark programs better:
Caution: Please complete the basics of Python first before jumping to this section. Make sure you are comfortable with following:

- [x] Variable, loops, conditional statements
- [x] Function definations in Python
- [x] lists and [list comprehensions](http://www.pythonforbeginners.com/basics/list-comprehensions-in-python)
- [x] Dictionaries
- [x] tuples 

#### Passing functions as argument to other functions:
Functions are first-class objects in python. you can pass them around, include them in dicts, lists, etc. Just don't include the parenthesis after the function name. 

Example:
```python
def best(x, criteria):
  """ A function that return best solution from list of solutions depending upon criteria"""
  return criteria(x)  # Once you add '()' around the variable name, python tries to run it as function.

def lowest(x):
  """ Return minimum from a list """
  return min(x)

def highest(x):
  """ Return maximum from a list"""
  return max(x)
  
# passing the functions around

# Will pass 'lowest()' function as an argument to other function
best([1,2,3,4], lowest)    # best() will return the '1' as best solution
best([1,2,3,4], highest)   # This time, the same function will return '4' as best solution

```

There are many in build function in Python that accepts other functions as output.
E.g map() function

```python
def square(x):
  return x**2
  
map(square, [1, 2, 3, 4])   # Will return [1, 4, 9, 16]
map(min, [1, 2, 3, 4])      # Will return 1
map(sum, [1, 2, 3, 4])      # will retun 10

```

**Tip:** Eventhough map() function is provided, the pythonic way to do above operations is via list comprehensions. The above ilustrations are just to meant to through some light on how we can pass functions as arguments to other functions.

#### args and Kwargs

`*args` (Variable preceeded with single astericks) and `**kwargs` (variable with double astericks) are used to pass variable number of arguments to function.

`*args` is used to pass list of arguments to function.

```python
def manyArgs(*args):
  print("I was called with", len(arg), "arguments:")
  print(args)

"""
>>> manyArgs(1, 2)
I was called with 1 arguments: 
(1, 2)
>>> manyArgs(1, 2, 3)
I was called with 3 arguments: 
(1, 2, 3)
"""
```

`**kwargs` is used to pass variable number of key-value arguments to function.

```python
def myfunc(**kwargs):
    # kwargs is a dictionary.
    for k,v in kwargs.iteritems():
         print("%s = %s" % (k, v))

"""
>>> myfunc(abc=123, efh=456)
abc = 123
efh = 456
"""
```

http://markmiyashita.com/blog/python-args-and-kwargs/

#### Understanding lambda functions in python:
 - Tutorial on lambdas: (http://www.python-course.eu/lambda.php) 
 - **Note:** Do not confuse this with lambda calculus. This is just a keyword for creating anonymous functions in Python. A shorcut for defining the throwaway functions. 
