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




1. **Numeric types**: Integers (int), floating-point numbers (float), and complex numbers (complex).
2. **Strings (str)**: A sequence of characters enclosed in single quotes (' ') or double quotes (" ").
3. **Lists (list)**: An ordered collection of elements, which can be of different types. Lists are mutable, meaning their values can be changed.
4. **Tuples (tuple)**: Similar to lists, but tuples are immutable, meaning their values cannot be modified once assigned.
5. **Dictionaries (dict)**: A collection of key-value pairs, where each value is associated with a unique key.
6. **Sets (set)**: An unordered collection of unique elements. Sets do not allow duplicate values.
7. **Boolean (bool)**: Represents the truth values True and False, often used in logical operations and conditional statements.

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
