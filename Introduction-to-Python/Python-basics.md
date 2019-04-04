1.Python-basics
===

1.1 The Python Interface
---
Instructions:
Trying to do some simple colculation on python.

You can type your code in the python script and to get the out put in the IPython shell.
python script:
       
       # Example, do not modify!
        print(5 / 8)

        # Put code below here
        print(7+10)

python IPythonshell:
        
        output:
        # Example, do not modify!
        print(5 / 8)
        
        # Put code below here
        print(7+10)
        0.625
        17

**' / ' equals division, ' - ' equals minus, ' + ' equals plus, ' * ' equals times.**

**Type print to show the outcome.**


1.2 Any comments?
---

To add comments to your Python script, you can use the # tag. **These comments are not run as Python code**, so they will not influence your result. As an example, take the comment on the right, # Division; it is completely ignored during execution.

Example:
code:
       
       # Division
       print(5 / 8)

       # Addition
       print(7 + 10)
       
outcome:

       # Division
        print(5 / 8)
        
       # Addition
        print(7 + 10)
        0.625
        17
        
And any'#'will not influence your result. They are just comments.

1.3 Python as calculator
---

Exponentiation: ** . This operator raises the number to its left to the power of the number to its right. For example 4 ** 2 will give 16.（算平方）

Modulo: %. This operator returns the remainder of the division of the number to the left by the number on its right. For example 18 % 7 equals 4.（取余）

Example:

Python script:

       # Addition, subtraction
       print(6 + 6)
       print(6 - 6)

       # Multiplication, division, modulo, and exponentiation
       print(6 * 5)
       print(20 / 2)
       print(15 % 7)
       print(8 ** 2)

       # How much is your $100 worth after 9 years?(10% return annually)
       print(100 * 1.1 ** 9)

IPythonshell:

       12
       0
       30
       10.0
       1
       64
       235.7947691000002

1.4 Variable Assignment
---

**Useing python you can type " = " to refer a value with a name. To creat a varialbe use " = ".**

Example:

Python script:

       # Create a variable savings
       savings = 100

       # Print out savings
       print(savings)

IPythonshell:

       100
       
**In python " = " means assignment not equality.**

1.5 Calculation with varialbe
---

Instead of calculating with actural number, we can calculating with variables.
Example:

Python script:

       # Create a variable savings
       savings = 100

       # Create a variable growth_multiplier
       growth_multiplier = 1.1

       # Calculate result

       result = savings * growth_multiplier ** 7
       
IPythonshell:

       194.87171000000012
       
1.6 Other variable types
---
Variable types in python.

- **int**, or integer: a number without a fractional part. savings, with the value 100, is an example of an integer.(整数）

- **float**, or floating point: a number that has both an integer and fractional part, separated by a point. growth_multiplier, with the value 1.1, is an example of a float.（带有小数点的数）

- **str**, or string: a type to represent text. You can use single or double quotes to build a string.（字符）

- **bool**, or boolean: a type to represent logical values. Can only be True or False (the capitalization is important!).（逻辑）

Example

Python script:

       # Create a int varialbe.
       integer = 10
       print(type(integer))

       # Create a float varialbe.
       integer_fractional = 10.0
       print(type(integer_fractional))

       # Create a str.
       desc = 'compound intersest'
       print(type(desc))

       # Create a boolean.
       profitable = True
       print(type(profitable))

       print(bool(integer > 10))

IPythonshell:
       
       <class 'int'>
       <class 'float'>
       <class 'str'>
       <class 'bool'>
       False
       


1.7 Operation with other types
---

What will you get when you sum two strings?
What will you get when you sum two booleans?

Example:

Python script:

       savings = 100
       growth_multiplier = 1.1
       desc = "compound interest"
       profit = True
       debt = False
       # Assign product of growth_multiplier and savings to year1
       year1 = savings * growth_multiplier

       # Print the type of year1
       print(type(year1))

       # Assign sum of desc and desc to doubledesc
       doubledesc = desc * 2

       # Print out doubledesc
       print(doubledesc)

       # Print out the sum of two profit
       print(profit*2)

       # Print out the sum of two debt
       print(debt*2)

       # Type of the sum pf two booleans
       print(type(profit*2))
       
IPythonshell:
       
       <class 'float'>
       compound interestcompound interest
       2
       0
       <class 'int'>
       
**The product of int and float always return a float.
The sum of two strings is simply add combined two strings together.
The sum of two booleans are int 2, True return int(1), false return int(0).
If you add or minus booleans you will get a int.**

1.8 Type conversion
---
Different types of varialbes can't used in the same sentence.
So we nead to convert their type to fit the syntax.

We can use floar() int() str() bool() to change their type.

Example 1.8.1: 

Python script:

       # Definition of savings and result
       savings = 100
       result = 100 * 1.10 ** 7


       # we convert int(savings) into str and float(result) into str
       print("I started with $" + str(savings) + " and now have $" + str(result) + ". Awesome!")

       # Definition of pi_string
       pi_string = "3.1415926"

       # Convert pi_string into float: pi_float
       pi_float = float(pi_string)
       print(pi_float)

IPythonshell:

       I started with $100 and now have $194.87171000000012. Awesome!
       3.1415926
       

**1.8.2 What is the result if we convert int, float and str into bool? or we convert bool to int, str and float?**

Python script:

       # Convert int to bool
       savings = 100 # int
       print(bool(savings))# convert int to bool

       # Convert float to bool
       returnn = 1.1 # float
       print(bool(returnn)) # convert float to bool

       # Convert str to bool
       result = '1000' # numerical str
       names = 'fc' # character str
       print(bool(result))
       print(bool(names))
IPythonshell:

       True
       True
       True
       True

Python script:

       # bool convert to int
       a = True
       print(int(a))

       # bool convert to float
       print(float(a))

       # bool convert to str
       print(str(a))

Ipythonshell:

       1
       1.0
       True
       
**Conclusion: Int, str and float can convert to bool, and the output is the same, it always return True for this convert.
Also bool can convert into int, float and bool. (True will return 1 or 1.0 when convert to int and float. Flase will return 0 or 0.0 for them.)**

**1.8.3 Can we convert character str to int and floar or bool?

Python script:

       # Convert str to int, float and bool
       a = 'a'
       int(a)
       float(a)
       bool(a)
IPthonshell:

       Traceback (most recent call last):
       File "<stdin>", line 3, in <module>
       int(a)
       ValueError: invalid literal for int() with base 10: 'a'
       
       Traceback (most recent call last):
        File "<stdin>", line 3, in <module>
       float(a)
       ValueError: could not convert string to float: 'a'
       True
       
**Conclustion: We can not convert character str to int and float, but can convert to bool and the result is True.


