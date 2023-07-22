# How python works
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Custom](https://badgen.net/badge/Custom?style=for-the-badge&logo=python&logoColor=ffdd54)

Python code is a high level code when executed gets converted to byte code through intrepreter in runtime line by line into a machine code and this is how the code runs.

## How to look at a source code of an existing python code
```
import inspect
import inspect
from re import findall

class Sample:
    def hello_python(self):
        return 'I am doing great'

# creating object of the class
samp = Sample()
# ways to look for the source code of the classs
print(inspect.getsource(type(samp)))
print(inspect.getsource(samp.__class__))
# way to look source code of a function of a class
print(inspect.getsource(samp.hello_python))
# getting source code for imported module
print(inspect.getsource(findall))
```
# [Dunder](https://docs.python.org/3/reference/datamodel.html#object.__repr__) Magic Methods

Methods having two prefix and suffix underscores in the method name. Dunder here means “Double Under (Underscores)”. These are commonly used for operator overloading. Few examples for magic methods are: __init__, __add__, __len__, __repr__ etc.

```
# declare our own string class
class String:
      
    # magic method to initiate object
    def __init__(self, string):
        self.string = string
          
# Driver Code
if __name__ == '__main__':
      
    # object creation
    string1 = String('Hello')
  
    # print object location
    print(string1)

OUTPUT - <__main__.String object at 0x7fe992215390>
```
The above snippet of code prints only the memory address of the string object. Let’s add a __repr__ method to represent our object.
```
# declare our own string class
class String:
      
    # magic method to initiate object
    def __init__(self, string):
        self.string = string
          
    # print our string object
    def __repr__(self):
        return 'Object: {}'.format(self.string)
  
# Driver Code
if __name__ == '__main__':
      
    # object creation
    string1 = String('Hello')
  
    # print object location
    print(string1)

OUTPUT - Object: Hello
```

# Decorators
# Generator 
A Generator in Python is a function that returns an iterator using the Yield keyword. An iterator in Python is an object that is used to iterate over iterable objects like lists, tuples, dicts, and sets. 

Generator and Iterators more or less same thing, doing the same thing behind the scenes. Generators are new way of defining iterator with new syntax from python 3X.

### When to use Generators
We use Generators in a scenario where we do not want all our value to get stored in the memory and then work upon them especially in the case where we are not intrested in the previous or next value but only intrested in current value.

**Examples where we can save memory and make our program run fast**
Incase of scenario where we are iterating over a iterable object (e.g list) and only intrested in current value of the iterable we should avoid using list but instead use range function in the for loop
```
import sys

# sample iterable (list)
x = [1, 2, 3, 4, 5]
# printing the size of list in memory
print(sys.getsizeof(x))
# prints 120

# doing the same thing with range
print(sys.getsizeof(range(1,6)))
# prints 48
```
Another example with map, we can use map as it does the operation on the iterable when called but not before that hence so use map wherever possible it will save memory and execution will be fast
```
import sys

# sample iterable (list)
x = [1, 2, 3, 4, 5]
# printing the size of list in memory
print(sys.getsizeof(x))
# prints - 120
y = map(lambda z: z-1, x)
# will give us the memory location but not the actual result
print(y)
# prints - <map object at 0x00000144CF533B80>
# so to get the result out of the mmap we need to call it and execute it in our program meaning map only executes
# when called otherwise does nothing
print(list(y))
# prints - [0, 1, 2, 3, 4]
# printing the size of list in memory
print(sys.getsizeof(list(y)))
# prints - 56
```
**Comparison of normal code with range and map**
```
Will do it using above example in some days
```

So basically the iterator functions which in our case if range and map is calling next method behind the scene to give us the current result and not bothering for the previous result and next result.

Now coming back to the concept of generators and how to implement it in python as said this is new way of calling or creating iterators from python 3x onwards we will use yield keyword in outr function to make it generator as shown in the example below
```
import sys

# sample iterable (list)
x = [1, 2, 3, 4, 5]
# printing the size of list in memory
print(sys.getsizeof(x))

# simple function to multiply the numbers
def multiply_the_numbers(x):
    for i in x:
        print(f'multiplied value is : {i**2}')

# calling the function
multiply_the_numbers(x)

# now creating the generator in above function
def multiply_the_numbers(x):
    for i in x:
        yield i**2

# calling the generator
value = multiply_the_numbers(x)
print(f'multiplied value is : {next(value)}')
print(f'multiplied value is : {next(value)}')

# or we can call it like below
for d in multiply_the_numbers(x):
    print(f'multiplied value is : {d}')

```
## Generator in comprehension
```
# inside the parenthesis you define the logic and hence the output becomes iterator
x = (i for i in range(10))
```

### Where we can use generators
    - Scenario where you want tp iterate overa a iterable and condition where previous and next value is not of much importance and you are intrested in only the current value
    - Scenario where you want to look for a specific condition in a large corpse of text - e.g specific keywords extraction from a huge file
    ```
    def read_csv_file(file_name):
        for line in open(file_name, 'r'):
            yield line
    ```

    





