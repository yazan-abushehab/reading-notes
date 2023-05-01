# List Comprehensions 
## why this topic matters as it relates to what you are studying in this module ?
List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.
Notes about Lists Comprehensions
>- List comprehension methods are an elegant way to create and manage lists. 
>- In Python, list comprehensions are a more compact way of creating lists. 
>- More flexible than for loops, list comprehension is usually faster than other methods.

<br>

## What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.
Python list comprehension is a concise and readable way to create a new list by applying an operation to each element of an existing list or iterable. 
List comprehension is often more concise and easier to read than using a for loop to create a list. It also tends to be faster and more efficient for smaller lists, although for larger lists the performance difference may be negligible.

Here's an example of a list comprehension that squares the elements in a given list of integers:

      numbers = [1, 2, 3, 4, 5]
      squares = [x**2 for x in numbers]
      print(squares)

To achieve the same result using a for loop, we would need to create an empty list and then use the append() method to add the squared elements to the list:

     numbers = [1, 2, 3, 4, 5]
     squares = []
     for x in numbers:
        squares.append(x**2)
     print(squares)

This produces the same output as the list comprehension example above. However, the list comprehension is more concise and easier to read.

<br>

# Primer on Decorators
## What is a decorator in Python?
In Python, a decorator is a special type of function that can be used to modify the behavior of other functions or classes. Decorators allow us to add functionality to existing code without modifying the original code itself. They are a powerful tool for code reuse and abstraction.

In Python, a decorator is defined using the @decorator_function syntax, where decorator_function is the name of the decorator function. A decorator function takes a function as its argument, and returns a new function that wraps the original function with some additional functionality.

<br>

## Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.
In Python, a decorator is a function that takes another function as input and returns a new function as output. The new function has the same name as the original function but is enhanced with additional functionality. Decorators are used to modify or extend the behavior of functions without changing their source code.

The way decorators work is by wrapping the original function with another function that adds extra functionality. This is done by defining a new function that takes the original function as an argument, defining the additional functionality in this new function, and returning a new function that combines the original and additional functionality.

Here is an example of a simple decorator that adds logging functionality to a function:

    def logger(func):
       def wrapper(*args, **kwargs):
          print(f"Function {func.__name__} was called with args {args} and kwargs {kwargs}")
          return func(*args, **kwargs)
       return wrapper

    @logger
    def my_function(x, y):
        return x + y

    result = my_function(1, 2)
    print(result)

<br>

## Things I want to know more about :
Nothing for now .