# How python works

Python code is a high level code when executed gets converted to byte code through intrepreter in runtime line by line into a machine code and this is how the code runs.

## How to look at a source code of an existing python code
```
import inspect

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
```




