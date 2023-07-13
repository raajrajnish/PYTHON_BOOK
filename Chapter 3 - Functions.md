# Chapter 3 - Functions

A function is a block of reusable code that performs a specific task. Functions allow you to break down your code into smaller, more manageable pieces, making it easier to read, understand, and maintain. 
They also promote code reusability and modularity.

Here's the general syntax for defining a function in Python:
```
def function_name(parameters):
    # Function body
    # Perform some operations
    # Return a value (optional)
```

Let's look at a simple example of a function that adds two numbers: Below we define a function called add_numbers that takes two parameters (a and b). Inside the function, we add the values of a and b and store the result in a variable called result. Finally, we use the return statement to send the result back as the output of the function.
```
def add_numbers(a, b):
    result = a + b
    return result
```
You can call this function by providing arguments for a and b:
```
sum_result = add_numbers(3, 5)
print(sum_result)  # Output: 8
```
Here's another example that demonstrates a function without any parameters: In this case, the say_hello function doesn't accept any parameters. It simply prints the string "Hello, World!" when called.
```
def say_hello():
    print("Hello, World!")

say_hello()  # Output: Hello, World!
```
You can also define default parameter values for a function. Here's an example:
```
def greet(name=""):
    if name:
        print(f"Hello, {name}!")
    else:
        print("Hello, stranger!")

greet()  # Output: Hello, stranger!
greet("Alice")  # Output: Hello, Alice!
```

In the above example, the greet function has a default parameter value of an empty string for the name parameter. If no argument is provided, it greets the user as a stranger. If an argument is passed, it greets the user by their name.



