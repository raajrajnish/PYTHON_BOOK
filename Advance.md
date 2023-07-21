# How python works

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
# [Dunder/Magic] Methods(https://docs.python.org/3/reference/datamodel.html#object.__repr__)

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
