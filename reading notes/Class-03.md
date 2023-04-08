# Read & Write Files in Python :
## why this topic matters as it relates to what you are studying in this module ?
One of the most common tasks that you can do with Python is reading and writing files. Whether it’s writing to a simple text file, reading a complicated server log, or even analyzing raw byte data, all of these situations require reading or writing a file.

<br>

## What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?
It’s important to remember that it’s your responsibility to close the file. In most cases, a file will be closed eventually. However, there is no guarantee when exactly that will happen. This can lead to unwanted behavior including resource leaks.

The with statement automatically takes care of closing the file once it leaves the with block, even in cases of error. as it allows for cleaner code and makes handling any unexpected errors easier for you.

<br>
<br>

# Exceptions in Python :
## why this topic matters as it relates to what you are studying in this module ?
The exception error is a type of error occurs whenever syntactically correct Python code results in an error. The last line of the message indicated what type of exception error you ran into.

<br>

## Explain the difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. Provide examples of when to use each method?
>- read(): This method reads the entire contents of a file and returns it as a string. If no argument is specified, it reads the entire file. If an integer argument n is given, it reads n characters from the file. When you call read() again, it will start from where it left off the previous time.

>-readline(): This method reads a single line from the file and returns it as a string. If you call it again, it reads the next line. When it reaches the end of the file, it returns an empty string.

### Here are some examples of when to use each method:
>- read(): If you need to read the entire contents of a small file into memory, you can use read(). For example:

<br>

    with open('myfile.txt', 'r') as f:

       contents = f.read()

<br>

>- readline(): If you're working with a large file and you only need to process one line at a time, you can use readline(). For example:

    with open('myfile.txt', 'r') as f:
     line = f.readline()
      while line:
        # process the line
        line = f.readline()

<br>
<br>

# File Objects - Reading and Writing to Files :
## Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.

In Python, exception handling is the process of dealing with errors or exceptional situations that can occur during the execution of a program. It is a way to handle errors gracefully and prevent the program from crashing.

The try, except, and finally blocks are used in Python for exception handling. Here's how they work:

>- try block: This block contains the code that might raise an exception. If an exception occurs, the code execution stops at the point where the exception occurred and moves to the corresponding except block.

>- except block: This block contains the code that should be executed when an exception occurs. It "catches" the exception and handles it in some way. You can specify the type of exception that the block should handle. If the exception type is not specified, the block will catch any exception.

>- finally block: This block contains the code that should be executed regardless of whether an exception occurred or not. It is executed even if there is a return, break, or continue statement in the try or except block.

<br>

Here is a simple example of how to use try, except, and finally blocks:

    try:
        x = int(input("Enter a number: "))
        y = int(input("Enter another number: "))
        result = x / y
        print("Result:", result)
    except ValueError:
        print("Invalid input!")
    except ZeroDivisionError:
        print("Cannot divide by zero!")
    finally:
        print("Program completed.")


In this example, the user is prompted to enter two numbers. The try block attempts to divide the first number by the second number. If either of the inputs is not a valid integer, a ValueError exception is raised and the code execution moves to the first except block. If the second input is zero, a ZeroDivisionError exception is raised and the code execution moves to the second except block. In either case, an error message is printed. Finally, the finally block is executed to print the completion message.

<br>

## Things I want to know more about :
Nothing for now .
