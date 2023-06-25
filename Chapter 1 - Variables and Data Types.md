## Chapter 1 - Variables and Data Types

Variables and data types are fundamental concepts in Python that allow you to store and manipulate different types of values within a program.

**1. Variables**: A variable is a named location in memory that holds a value. It allows you to store and refer to data during program execution. In Python, you can declare a variable by assigning a value to it using the assignment operator (=). 

For example:

```
x = 179
name = "Hi i am learning python to get started in ML"
```

In this example, the variable name is assigned the value of the string "John Doe". The value of the variable can be changed later in the program, but the name of the variable cannot be changed.

Variables in Python have a few important properties:

  - **Names**: Variable names must start with a letter or underscore, and they can only contain letters, numbers, and underscores.
  - **Scope**: The scope of a variable is the part of the program where the variable is visible. Variables that are defined in the global scope are visible   throughout the entire program, while variables that are defined in a function scope are only visible within the function.
  - **Type**: Variables can hold different types of values, such as integers, floats, strings, lists, and dictionaries. The type of a variable is determined by the value that is assigned to it.

**2. Data Types**: Python has several built-in data types, which define the nature of the values that can be stored in variables. Here is a table of the different types of variables in Python:

Serial| Type | Shortform | Description|
--- |--- | ---| ---|
1 |**Integer** |int         | A whole number, such as 1, 2, or 3.
2 |**Float** |float         | A number with a decimal point, such as 1.0, 2.5, or 3.14159.
3 |**String**|str           | A sequence of characters, enclosed in single quotes (' ') or double quotes (" "), such as "Hello, world!" or "This is a string."
4 |**List**|list            | A sequence of objects or An ordered collection of elements, which can be of different types. Lists are mutable, meaning their values can be   changed.such as [1, 2, 3, 4, 5].
5 |**Tuple**|tuple          | Similar to lists, a sequence of objects that is immutable, meaning that it cannot be changed once it is created.
6 |**Set**|set              | An unordered collection of unique elements. Sets do not allow duplicate values.
7 |**Dictionary**|dict      | A collection of key-value pairs, where each value is associated with a unique key.
8 | **Boolean**|bool        | Represents the truth values True and False, often used in logical operations and conditional statements.


**3. Type Inference**: In Python, you don't need to explicitly declare the data type of a variable. The interpreter dynamically infers the type based on the assigned value. 

For example:

```
x = 179
name = "Hi i am learning python to get started in ML"
```

**4. Type Conversion (Type Casting)**: You can convert between different data types using type conversion functions like int(), float(), str(), etc. 

For example:

```
x = int("10")  # Convert string "10" to an integer
y = float(5)   # Convert integer 5 to a float
```

Understanding variables and data types is essential for effectively storing and manipulating data in Python programs.

**Section 1 Integers**

Integers, in Python, are a data type used to represent whole numbers without any decimal points. They can be positive, negative, or zero. Here's an explanation of integers with some examples in Python:

 - **Declaring Integers**: You can assign integer values to variables using the assignment operator (=). 
      ```
      x = 10
      y = -5
      z = 0
      ```
- **Arithmetic Operations**: Integers support various arithmetic operations, such as addition (+), subtraction (-), multiplication (*), division (/), and modulus (%).
    ```
    a = 10 + 5    # Addition: a becomes 15
    b = 10 - 5    # Subtraction: b becomes 5
    c = 10 * 5    # Multiplication: c becomes 50
    d = 10 / 5    # Division: d becomes 2.0 (float)
    e = 10 % 3    # Modulus: e becomes 1 (remainder of division)
    ```
 - **Integer Division**: The double forward slash operator (//) performs integer division, which returns the quotient as an integer, discarding any decimal remainder
     ```
     quotient = 10 // 3   # quotient becomes 3
     ```
- **Exponentiation**: The double asterisk operator (**) raises an integer to a power.
    ```
    result = 2 ** 3   # result becomes 8 (2 raised to the power of 3)
    ```
- **Type Conversion**: You can convert other data types to integers using the int() function.
   ```
    x = int("10")    # x becomes 10 (string to integer conversion)
    y = int(3.14)    # y becomes 3 (float to integer conversion)
    ```
- **Integer Operations**: In Python, integers follow the rules of integer operations. For instance, division between two integers always returns a float, even if the result is a whole number. To get the integer division result, you can use the integer division operator (//).
   ```
    a = 10 / 5   # a becomes 2.0 (float division)
    b = 10 // 5  # b becomes 2 (integer division)
    ```

Integers are commonly used for counting, indexing, and performing mathematical operations in Python. They are a fundamental data type that allows you to represent and work with whole numbers efficiently.

**Section 2 Floats**

Floats, short for floating-point numbers, are a data type in Python used to represent decimal numbers. They are used when more precision or fractional values are required. Here's an explanation of floats with some examples in Python:

- **Declaring Floats**: Float values can be assigned to variables using the assignment operator (=).
    ```
    x = 3.14
    y = -2.5
    z = 0.0
    ```
- **Arithmetic Operations**: Floats support the same arithmetic operations as integers, including addition (+), subtraction (-), multiplication (*), division (/), and modulus (%).
    ```
    a = 3.14 + 1.5    # Addition: a becomes 4.64
    b = 3.14 - 1.5    # Subtraction: b becomes 1.64
    c = 3.14 * 2.0    # Multiplication: c becomes 6.28
    d = 3.14 / 2.0    # Division: d becomes 1.57
    e = 3.14 % 2.0    # Modulus: e becomes 1.14 (remainder of division)
    ```
- **Type Conversion**: Floats can be converted to integers using the int() function. This conversion truncates the decimal part and returns the whole number part.
    ```
    x = int(3.14)    # x becomes 3 (float to integer conversion)
    y = int(5.99)    # y becomes 5 (float to integer conversion)
    ```
- **Float Precision**: Floats have a finite precision and may not always be exact. This is due to the nature of floating-point representation in computer systems. Therefore, it's important to be aware of potential precision issues when performing calculations with floats.
    ```
    a = 0.1 + 0.2
    print(a)   # Output: 0.30000000000000004 (not exactly 0.3 due to precision limitations)
    ```
Floats are commonly used in scientific calculations, financial applications, and anywhere precise decimal values are required. They provide the flexibility to work with numbers that include fractional parts and allow for more precise calculations than integers.



    
