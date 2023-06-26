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


**Section 3 Strings**

Strings in Python are a data type used to represent a sequence of characters. They are enclosed in either single quotes (' ') or double quotes (" "). Here's an explanation of strings with some examples in Python:

- **Declaring Strings**: Strings can be assigned to variables using the assignment operator (=). 
    ```
    name = "John"
    message = 'Hello, world!'
    ```
- **String Concatenation**: Strings can be concatenated (joined) using the plus operator (+), which combines the characters of two or more strings into a single string. 
    ```
    greeting = "Hello, " + name + "!"
    ```
- **Accessing Characters**: Individual characters within a string can be accessed using indexing. In Python, indexing starts from 0, so the first character of a string is at index 0.
    ```
    text = "Hello"
    first_char = text[0]    # first_char becomes 'H'
    ```
- **String Slicing**: You can extract a portion of a string using slicing. Slicing allows you to specify a range of indices and retrieve the characters within that range.
    ```
    text = "Hello, world!"
    sub_text = text[7:12]    # sub_text becomes "world"
    ```
- **String Length**: The len() function returns the length (number of characters) of a string.
    ```
    text = "Hello"
    length = len(text)    # length becomes 5
    ```
- **String Methods**: Python provides numerous built-in string methods that allow you to manipulate and modify strings. Some commonly used string methods include:
   - lower(): Converts a string to lowercase.
   - upper(): Converts a string to uppercase.
   - strip(): Removes leading and trailing whitespace from a string.
   - split(): Splits a string into a list of substrings based on a delimiter.
   - replace(): Replaces occurrences of a substring with another substring.
   - find(): Searches for the first occurrence of a substring within a string and returns its index.
   - count(): Counts the number of occurrences of a substring in a string.

- **String Formatting**: Python provides several ways to format strings, including the format() method and formatted string literals (f-strings). These methods allow you to insert variables and expressions into strings dynamically.
    ```
   name = "Alice"
   age = 25
   message = "My name is {} and I am {} years old.".format(name, age)
    ```
**Section 4 List**

In Python, a list is a versatile and commonly used data structure that allows you to store and organize multiple items in a single variable. Lists are mutable, which means you can modify them by adding, removing, or modifying elements. Each element within a list has a specific index that represents its position.

Here's an explanation of lists with some examples in Python:

Strings are widely used in Python for representing text-based data, working with user input, formatting output, and much more. They are versatile and provide various methods and operations for string manipulation.

- **Creating a List**: To create a list, enclose comma-separated values within square brackets []
    ```
   fruits = ['apple', 'banana', 'orange', 'mango']
    ```
- **Accessing List Elements**: You can access individual elements of a list using their index. Remember, indexing starts from 0.
    ```
   print(fruits[0])  # Output: 'apple'
   print(fruits[2])  # Output: 'orange'
    ```
- **Modifying List Elements**: Lists are mutable, so you can modify elements by assigning new values to specific indices. 
    ```
  fruits[1] = 'grape'
  print(fruits)  # Output: ['apple', 'grape', 'orange', 'mango']
    ```
- **List Length**: You can determine the length (number of elements) in a list using the len() function. 
    ```
    print(len(fruits))  # Output: 4
    ```
- **Adding Elements to a List**: You can append elements to the end of a list using the append() method.
    ```
    fruits.append('pineapple')
    print(fruits)  # Output: ['apple', 'grape', 'orange', 'mango', 'pineapple']
    ```
- **Removing Elements from a List**: You can remove elements from a list using methods like remove() or pop(). 
    ```
    fruits.remove('orange')
    print(fruits)  # Output: ['apple', 'grape', 'mango', 'pineapple']
    
    popped_fruit = fruits.pop(0)
    print(popped_fruit)  # Output: 'apple'
    print(fruits)  # Output: ['grape', 'mango', 'pineapple']
    ```
- **Slicing a List**: You can extract a portion of a list using slicing, which specifies a range of indices
    ```
    print(fruits[1:3])  # Output: ['grape', 'mango']
    print(fruits[:2])  # Output: ['grape', 'mango']
    print(fruits[2:])  # Output: ['mango', 'pineapple']
    ```
Lists are incredibly versatile and offer various built-in methods for sorting, searching, and manipulating elements. By using lists, you can efficiently store and work with collections of data in Python.

**Section 5 Tuple**

In Python, a tuple is a data structure similar to a list but with one key difference: tuples are immutable, meaning they cannot be modified once created. Tuples are often used to store related pieces of information together and provide a way to ensure the integrity of the data. Tuples are defined using parentheses ().

- **Creating a Tuple**: To create a tuple, enclose comma-separated values within parentheses ().
    ```
     person = ('John', 25, 'USA')
    ```
- **Accessing Tuple Elements**: You can access individual elements of a tuple using indexing, just like with lists. The indexing starts from 0.
    ```
     print(person[0])  # Output: 'John'
     print(person[1])  # Output: 25
    ```
- **Tuple Unpacking**: You can assign tuple elements to separate variables using tuple unpacking. This allows you to conveniently access individual elements without using indexing.
    ```
     name, age, country = person
     print(name)     # Output: 'John'
     print(age)      # Output: 25
     print(country)  # Output: 'USA'
    ```
- **Immutable Nature**: Unlike lists, tuples are immutable. Once created, you cannot modify the elements of a tuple. 
    ```
    person[1] = 30  # Error: Tuples are immutable
    ```
- **Tuple Length**: You can determine the length (number of elements) in a tuple using the len() function. 
    ```
    print(len(person))  # Output: 3
    ```
- **Combining Tuples**: You can combine tuples using the concatenation operator (+) to create a new tuple. 
    ```
    tuple1 = (1, 2, 3)
    tuple2 = ('a', 'b', 'c')
    combined_tuple = tuple1 + tuple2
    print(combined_tuple)  # Output: (1, 2, 3, 'a', 'b', 'c')
    ```
- **Tuple as Return Values**: Tuples are commonly used to return multiple values from a function.
    ```
    def get_coordinates():
    x = 10
    y = 20
    return x, y

    x_coord, y_coord = get_coordinates()
    print(x_coord)  # Output: 10
    print(y_coord)  # Output: 20
    ```
Tuples provide a convenient way to store related data that should not be modified. They are commonly used in scenarios where data integrity and immutability are desired, such as when passing data between functions or representing fixed sets of values.

**Section 6 Set**

In Python, a set is an unordered collection of unique elements. Sets are used to store distinct items and perform operations like union, intersection, and difference efficiently. Sets are defined using curly braces {} or the set() constructor.

- **Creating a Set**: To create a set, enclose comma-separated values within curly braces {}. 
    ```
    fruits = {'apple', 'banana', 'orange'}
    ```
- **Adding Elements to a Set**: You can add elements to a set using the add() method.
    ```
    fruits.add('mango')
    print(fruits)  # Output: {'apple', 'banana', 'orange', 'mango'}
    ```
- **Removing Elements from a Set**: You can remove elements from a set using methods like remove() or discard(). 
    ```
    fruits.remove('banana')
    print(fruits)  # Output: {'apple', 'orange'}
    
    fruits.discard('grape')
    print(fruits)  # Output: {'apple', 'orange'}
    ```
- **Set Operations**: Sets support various operations like union, intersection, and difference.
    - **Uniom**: Combines elements from two sets into a new set using the union() method or the | operator.
      ```
        set1 = {1, 2, 3}
        set2 = {3, 4, 5}
        union_set = set1.union(set2)
        print(union_set)  # Output: {1, 2, 3, 4, 5}
      ```
        
  - **Intersection**: Retrieves common elements between two sets using the intersection() method or the & operator.
    ```
        set1 = {1, 2, 3}
        set2 = {3, 4, 5}
        intersection_set = set1.intersection(set2)
        print(intersection_set)  # Output: {3}
    ```
    
  - **Difference**: Retrieves elements present in one set but not in the other using the difference() method or the - operator. 

    ```
        set1 = {1, 2, 3}
        set2 = {3, 4, 5}
        difference_set = set1.difference(set2)
        print(difference_set)  # Output: {1, 2}
    ```
- **Set Membership**: You can check if an element is present in a set using the in keyword.
    ```
    if 'apple' in fruits:
      print("Apple is in the set")
    ```
    
- **Set Length**: You can determine the number of elements in a set using the len() function.
    ```
    print(len(fruits))  # Output: 2
    ```
Sets are useful when you want to work with unique elements and perform operations based on set theory. They provide efficient methods for manipulating and comparing sets of data in Python.

**Section 7 Dictionary**

In Python, a dictionary is a data structure that allows you to store and retrieve data in key-value pairs. Dictionaries are mutable and unordered, meaning that the elements are not stored in a specific order. Each element in a dictionary is accessed by its key rather than an index.

- **Creating a Dictionary**: To create a dictionary, enclose key-value pairs within curly braces {} and separate them with colons (:).
    ```
    student = {'name': 'John', 'age': 25, 'country': 'USA'}
    ```
- **Accessing Dictionary Elements**: You can access individual elements of a dictionary by specifying their corresponding key. 
    ```
    print(student['name'])  # Output: 'John'
    print(student['age'])   # Output: 25
    ```
- **Modifying Dictionary Elements**: Dictionaries are mutable, so you can modify the value of an existing key or add new key-value pairs. 
    ```
    student['age'] = 26
    student['grade'] = 'A'
    print(student)  # Output: {'name': 'John', 'age': 26, 'country': 'USA', 'grade': 'A'}
    ```
- **Removing Dictionary Elements**: You can remove elements from a dictionary using the del keyword or the pop() method.
    ```
    del student['country']
    print(student)  # Output: {'name': 'John', 'age': 26, 'grade': 'A'}
    
    removed_value = student.pop('age')
    print(removed_value)  # Output: 26
    print(student)        # Output: {'name': 'John', 'grade': 'A'}
    ```
- **Dictionary Length**: You can determine the number of key-value pairs in a dictionary using the len() function. 
    ```
    print(len(student))  # Output: 2
    ```
- **Dictionary Keys and Values**:You can retrieve all the keys or values from a dictionary using the keys() and values() methods, respectively. 
    ```
    keys = student.keys()
    values = student.values()
    print(keys)   # Output: ['name', 'grade']
    print(values) # Output: ['John', 'A']
    ```
- **Checking Key Existence**:You can check if a key exists in a dictionary using the in keyword. 
    ```
    if 'name' in student:
    print("Name exists in the dictionary")
    ```
Dictionaries are versatile and commonly used for mapping data with meaningful associations. They provide a convenient way to store and access data using descriptive keys rather than numeric indices, making them suitable for various applications in Python.

**Section 8 Boolean**

In Python, a boolean is a data type that represents one of two possible values: True or False. Booleans are used to perform logical operations and make decisions based on the evaluation of conditions.

- **Boolean Values**: The boolean values in Python are True and False. They are case-sensitive, so make sure to capitalize the first letter.
    ```
    is_active = True
    is_registered = False
    ```
- **Boolean Operations**: Booleans can be combined and manipulated using logical operators such as and, or, and not. These operators allow you to perform logical operations on boolean values.
    ```
    a = True
    b = False
    
    print(a and b)   # Output: False
    print(a or b)    # Output: True
    print(not a)     # Output: False
    ```
- **Comparison Operators**: Comparison operators such as == (equal to), != (not equal to), < (less than), > (greater than), <= (less than or equal to), and >= (greater than or equal to) return boolean values based on the comparison result.
    ```
    x = 5
    y = 10
    
    print(x == y)    # Output: False
    print(x < y)     # Output: True
    print(x >= y)    # Output: False
    ```
- **Boolean Functions and Methods**: Python provides built-in functions and methods to work with booleans.
    ```
    # Built-in functions
    print(bool(0))           # Output: False
    print(bool(10))          # Output: True
    print(bool("Hello"))     # Output: True
    print(bool(""))          # Output: False
    
    # Methods
    fruits = ["apple", "banana", "orange"]
    print(fruits.__contains__("apple"))     # Output: True
    print(fruits.__contains__("grape"))     # Output: False
    ```
- **Boolean Conditions**: Booleans are commonly used in conditional statements, such as if statements, to control the flow of the program based on the evaluation of conditions.
    ```
    is_raining = True

    if is_raining:
        print("Remember to take an umbrella.")
    else:
        print("Enjoy the sunshine!")
    ```
Booleans are fundamental for making decisions and performing logical operations in Python. They are essential in control structures, conditionals, and expressing true/false conditions in various programming scenarios.
