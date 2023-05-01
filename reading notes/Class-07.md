# Python Scope :
## why this topic matters as it relates to what you are studying in this module ?
you’ve learned how a Python scope works and how they restrict the visibility of variables, functions, classes, and other Python objects to certain portions of your code. You now know that you can access or reference global names from any place in your code, but they can be modified or updated from within the global Python scope.

You also know that you can access local names only from inside the local Python scope they were created in or from inside a nested function, but you can’t access them from the global Python scope or from other local scopes. Additionally, you’ve learned that nonlocal names can be accessed from inside nested functions, but they can’t be modified or updated from there.

<br>

## Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.
In Python, variable scope refers to the part of a program where a variable can be accessed. The scope determines the visibility and accessibility of a variable. Variables can be defined in different scopes, such as the global scope or a local scope.

In Python, a variable declared inside a function has local scope, which means it can only be accessed within that function. Local variables are created when the function is called and are destroyed when the function exits. On the other hand, a variable declared outside of a function has global scope, which means it can be accessed from anywhere in the program.

Here is an example to illustrate the difference between local and global scope:

   x = 10

    def foo():
       # Local scope variable
       y = 5
       print("x inside function:", x) # accessing global variable
       print("y inside function:", y) # accessing local variable

    foo()
       print("x outside function:", x) # accessing global variable
       print("y outside function:") # This will cause an error since y is not defined in global scope

So, in summary, local variables have scope only within the function they are defined in, while global variables can be accessed from any part of the program. It is important to note that modifying a global variable inside a function requires using the global keyword to indicate that the variable being referred to is the global one, rather than creating a new local variable with the same name.

<br>

## How do the global and nonlocal keywords work in Python, and in what situations might you use them?
In Python, the global and nonlocal keywords are used to access variables that are defined outside the current function's scope.

The global keyword is used to indicate that a variable is a global variable, meaning it is defined in the global scope and can be accessed and modified from anywhere in the program. When a variable is modified inside a function using the global keyword, the change will affect the global variable, not create a new local variable.

We use the global and nonlocal keywords when we want to modify variables that are defined outside the current function's scope. However, it is generally best practice to minimize the use of global and nonlocal variables, as they can make the code harder to understand and maintain, and can introduce unexpected side effects.

<br>

# Big O notation is simpler than you might think :
## In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.
Big O notation is a way to describe the time and space complexity of algorithms and how their performance scales with input size. It's important to understand algorithmic complexity because it helps us identify the most efficient algorithms for a given problem and predict how they will perform on larger inputs.

The purpose of using Big O notation is to provide a standardized way of comparing the performance of different algorithms. It allows us to abstract away implementation details and focus on the growth rate of the algorithm as the input size increases. This helps us make informed decisions about which algorithm to choose for a given problem.

<br>

## Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.
To simulate a dice roll using Python, we can use the random module, which provides various functions for generating random numbers. We can use the randint() function to generate a random integer between 1 and 6, which simulates the roll of a single dice.

Here's an example of how to simulate a dice roll in Python:

       import random
       roll = random.randint(1, 6)
       print("The dice rolled:", roll)

To calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials, we can use a loop to simulate multiple dice rolls and count the number of times the desired outcome occurs. We can then divide the number of occurrences by the total number of trials to get an estimate of the probability.

Here's an example of how to calculate the probability of rolling a 6 over 1000 trials:

    import random
    #Simulate 1000 dice rolls and count the number of 6s
    num_trials = 1000
    num_sixes = 0

    for i in range(num_trials):
       roll = random.randint(1, 6)
       if roll == 6:
          num_sixes += 1

    #Calculate the probability of rolling a 6
    probability = num_sixes / num_trials
    print("The probability of rolling a 6 is:", probability)

In this example, we use a for loop to simulate 1000 dice rolls and count the number of times a 6 is rolled. We then divide the number of 6s by the total number of trials to get an estimate of the probability of rolling a 6.

By increasing the number of trials, we can get a more accurate estimate of the probability. We can also calculate the probability of rolling other numbers by changing the if statement inside the loop. For example, to calculate the probability of rolling a 1, we would change if roll == 6 to if roll == 1.

<br>

## Things I want to know more about :
Nothing for now .