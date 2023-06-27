# Chapter 2 - Control Flow

Control flow is the order in which the statements in a Python program are executed. It is what allows a program to make decisions and take different paths depending on the input or the state of the program.

- **Conditional Statements (if-else)**
    - If statements allow you to execute a block of code if a certain condition is met.
    - Else statements allow you to execute a block of code if the condition in the if statement is not met.
    - Elif statements allow you to chain multiple conditions together.

    Example 1
    ```
    In the below example, the program checks the value of variable x. If it's greater than 0, it prints "Positive number".
    If it's less than 0, it prints "Negative number". Otherwise, if it's equal to 0, it prints "Zero".
    
    x = 10
    
    if x > 0:
        print("Positive number")
    elif x < 0:
        print("Negative number")
    else:
        print("Zero")
    ```

    Example 2
    ```
    The following code will print "The number is even" if the number variable is even, "The number is positive"
    if the number variable is positive but not even, and "The number is negative" if the number variable is negative:
    
    number = 11
    
    if number % 2 == 0:
        print("The number is even")
    elif number > 0:
        print("The number is positive")
    else:
        print("The number is negative")
    ```

- **For Loop**
    - For loops allow you to execute a block of code a certain number of times.

    Example 1
    ```
    In the below example, the program iterates over the list of fruits and prints each fruit on a separate line.
    
    fruits = ['apple', 'banana', 'orange']
    
    for fruit in fruits:
        print(fruit)
    ```

  Example 2
  ```
   In the below example, the following code will print the numbers from 1 to 10:

  for i in range(1, 11):
    print(i)
  ```

    
- **While Loop**:
    - While loops allow you to execute a block of code as long as a certain condition is met.

    Example 1
    ```
    In the below example, the program prints the value of count and increments it by 1 in each iteration until count reaches 5.
    
    count = 0
    
    while count < 5:
        print(count)
        count += 1
    ```
    Example 2
    ```
    In the below example,  the following code will print the numbers from 1 to 10, but will stop if the number variable is equal to 5.
    
    count = 0
    
    while count < 5:
        print(count)
        count += 1
    ```

- **Break and Continue Statements**: In the below example, the program iterates over the list of numbers. If the current number is equal to 3, the loop is terminated using the break statement. If the number is even, the continue statement skips the current iteration. Only odd numbers (1 and 5) are printed.

```
numbers = [1, 2, 3, 4, 5, 6]

for num in numbers:
    if num == 3:
        break
    if num % 2 == 0:
        continue
    print(num)
```
- **Function Calls**:In the below example, a function called greet is defined. It takes a parameter name and prints a personalized greeting. The function is then called with the argument "Alice", resulting in the output "Hello, Alice!".

```
def greet(name):
    print("Hello, " + name + "!")

greet("Alice")
```

These examples demonstrate different aspects of control flow in Python, including conditional statements, loop structures, and function calls. By utilizing control flow, you can make decisions, repeat actions, and control the overall flow and behavior of your program.


  
