# Python [Class](https://docs.python.org/3.11/glossary.html#term-class)

A template for creating user-defined objects. Class definitions normally contain method definitions which operate on instances of the class.

## Naming Convention [PEP 8](https://peps.python.org/pep-0008/#class-names)

Type | Description|
--- |--- |
**Class** | Names should normally use the CapWords convention.
**Method/Function/Variable Names and Instance Variables** | Name should be lowercase, with words separated by underscores as necessary to improve readability.
**-**| If a function argument’s name clashes with a reserved keyword, it is generally better to append a single trailing underscore rather than use an abbreviation or spelling corruption. Thus class_ is better than clss.
**Instance methods**| Always use self for the first argument to instance methods.
**Class methods**| Always use cls for the first argument to class methods.
**Global Variable**| Global Variable Names, same as those for functions.
**Non-Public Methods and Instance Variables**| Use one leading underscore only for non-public methods and instance variables.
**-**| To avoid name clashes with subclasses, use two leading underscores to invoke Python’s name mangling rules.
**Constants**| Constants are usually defined on a module level and written in all capital letters with underscores separating words. Examples include MAX_OVERFLOW and TOTAL.

## Optional Paramters

## Static Class vs Class Method
to you class method we do not require to create object or instance of the class we can use it directly using the class namefollowed by period and then class name

## Map Function
The map() function is a built-in higher-order function that applies another function to each element of an iterable (e.g., list, tuple, etc.) and returns an iterator that yields the results. It is a way of transforming or processing data without using explicit loops.
```
map(function, iterable)
```
where:
function: This is the function that you want to apply to each element of the iterable. It can be a built-in function, a user-defined function, or a lambda function.
iterable: This is the collection of elements (e.g., list, tuple) on which you want to apply the function.

The map() function takes each element from the iterable, passes it as an argument to the specified function, and collects the results in an iterator.
In this below example, the double() function takes an input x and returns x * 2. The map() function applies this function to each element of the numbers list and returns an iterator with the results, which we then convert to a list for easy viewing.
```
def double(x):
    return x * 2

numbers = [1, 2, 3, 4, 5]
doubled_numbers = map(double, numbers)

# Convert the iterator to a list to see the results
result = list(doubled_numbers)
print(result)  # Output: [2, 4, 6, 8, 10]
```
In addition to using a named function like double(), you can also use lambda functions with map() to achieve concise and inline transformations:
```
numbers = [1, 2, 3, 4, 5]
doubled_numbers = map(lambda x: x * 2, numbers)

result = list(doubled_numbers)
print(result)  # Output: [2, 4, 6, 8, 10]
```
## Filter Function

The filter() function is another built-in higher-order function that is used to filter elements from an iterable (e.g., list, tuple) based on a given function, which acts as a filter. It returns an iterator containing only the elements for which the filter function evaluates to True.
```
filter(function, iterable)
```

where:
function: This is the filter function that returns a Boolean value (True or False) for each element in the iterable. Elements for which the function returns True will be included in the output, and elements for which it returns False will be excluded.
iterable: This is the collection of elements (e.g., list, tuple) from which you want to filter the elements.

In this below example, the is_even() function checks if a number x is even by evaluating the expression x % 2 == 0, which returns True for even numbers and False for odd numbers. The filter() function applies this filter function to each element of the numbers list and returns an iterator with the elements that pass the filter, which we then convert to a list for easy viewing.

```
def is_even(x):
    return x % 2 == 0

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_numbers = filter(is_even, numbers)

# Convert the iterator to a list to see the results
result = list(even_numbers)
print(result)  # Output: [2, 4, 6, 8, 10]
```
Similar to the map() function, you can use a lambda function with filter() for more concise filtering:
```
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_numbers = filter(lambda x: x % 2 == 0, numbers)

result = list(even_numbers)
print(result)  # Output: [2, 4, 6, 8, 10]
```

The filter() function is handy when you want to extract specific elements from a collection based on certain conditions, and it's an effective way to avoid writing explicit loops for filtering operations.


