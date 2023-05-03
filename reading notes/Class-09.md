# Dunder Methods :
## why this topic matters as it relates to what you are studying in this module ?
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

<br>

## What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method.
In Python, dunder methods (double underscore methods) are special methods that have predefined names and are used to define behaviors for specific operations. These methods are also known as magic methods, because they are invoked implicitly by Python in response to certain language-specific operations or syntax.

Dunder methods are often used to customize the behavior of Python built-in functions, operators, and statements, making it possible to create classes that mimic the behavior of built-in types, or that have specialized semantics.

For example, the __len__ method is a commonly used dunder method that defines the behavior of the len() built-in function when applied to an object of a custom class. The __len__ method should return the length of the object, as an integer value.

Here's an example of how to define the __len__ method in a custom class:

    class MyList:
       def __init__(self, items):
           self.items = items
    
       def __len__(self):
           return len(self.items)

# Statistics - Probability :
## why this topic matters as it relates to what you are studying in this module ?
When studying statistics for data science, you will inevitably have to learn about probability. It is easy lose yourself in the formulas and theory behind probability, but it has essential uses in both working and daily life.

<br>

## Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation.
The statistics module is a built-in Python module that provides functions for performing statistical calculations. The module contains functions for calculating various measures of central tendency (mean, median, mode), measures of variability (variance, standard deviation), and other statistical metrics.

Here is an example of a function in the statistics module:

    import statistics

    data = [1, 2, 3, 4, 5]

    mean = statistics.mean(data)
    print("Mean:", mean)

    median = statistics.median(data)
    print("Median:", median)

    mode = statistics.mode(data)
    print("Mode:", mode)

    variance = statistics.variance(data)
    print("Variance:", variance)

    stdev = statistics.stdev(data)
    print("Standard deviation:", stdev)

<br>

# AI Guru makes $238,800 with misleading paid course. doesn’t credit developers
## In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?
In the video "AI Guru makes $238,800 with misleading paid course," the main ethical issue raised concerned the use of developers' work without proper attribution or compensation. The AI guru in question allegedly used code from open-source repositories and online forums, claimed it as his own, and incorporated it into his paid course without giving credit to the original authors or contributors. This was seen as an unethical practice because it violated the principles of intellectual property rights, academic honesty, and fair use of resources.

To avoid this ethical issue, the AI guru could have taken several steps. Firstly, he could have acknowledged the sources of his code and given credit to the original authors or contributors. This could have been done through proper citations, references, or acknowledgments. Secondly, he could have obtained permission from the original authors or contributors to use their code and agreed on appropriate terms of use, such as licensing, attribution, or compensation. Thirdly, he could have developed his own code from scratch or hired developers to create original content for his course, rather than relying on other people's work. By doing so, he could have ensured that his course was based on legitimate, ethical, and sustainable practices that respect the rights and interests of all stakeholders.

<br>

## Things I want to know more about :
Nothing for now .