Logic control and filtering
===

1.1 Equality
---

Using == to check if two varialbes are equal or not.
Using != to check ineuquality.

Example

*Python script*
```
# Comparison of booleans
print(True == False)

# Comparison of integers
print(-5 * 15 != 75)

# Comparison of strings
print('pyscript' == 'PyScript')

# Compare a boolean with an integer
print(True == 1)
```

*IPythonshell*
```
<script.py> output:
    False
    True
    False
    True
```

1.2 Greater and less than
---

Using > and < to compare two varialbes.
Always remember >= and <= area valid syntax, =< and => are not.

Example

*Python script*
```
# Comparison of integers
x = -3 * 6
print(x >= -10)

# Comparison of strings
y = "test"
print('test' <= y)

# Comparison of booleans
print(True > False)
```

*IPythonshell*
```

<script.py> output:
    False
    True
    True
```

1.3 Compare Arrays
---

You can also use comparison operator in numpy array.
To compare numpy array.

Example

*Python script*
```
# Create arrays
import numpy as np
my_house = np.array([18.0, 20.0, 10.75, 9.50])
your_house = np.array([14.0, 24.0, 14.25, 9.0])

# my_house greater than or equal to 18
print(my_house >= 18)

# my_house less than your_house
```

*IPythonshell*
```

<script.py> output:
    [ True  True False False]
    [False  True  True False]
```

1.4 and or, not
---

A boolean is either 1 or 0, True or False.
Using boolean operator in your coding.

T and T is T
T and F is F
F and T is F
F and F is F

T or T is T 
T or F is T 
F or T is T
F or F is F

not T is F
not F is T

Example

*Python script*
```
# Define variables
my_kitchen = 18.0
your_kitchen = 14.0

# my_kitchen bigger than 10 and smaller than 18?
print(my_kitchen > 10 and my_kitchen < 18)

# my_kitchen smaller than 14 or bigger than 17?
print(my_kitchen > 14 or my_kitchen >17)

# Double my_kitchen smaller than triple your_kitchen?
print(my_kitchen*2 < your_kitchen*3)
```
*IPythonshell*
```
<script.py> output:
    False
    True
    True
```

1.5 Boolean Operators with numpy
---

Using boolean operators with numpy.
Unlike before, you can not use and, or, not on numpy 
Instead use np.logical_and, np.logical_or, np_logical_not with numpy.

Example

*Python script*
```
# Create arrays
import numpy as np
my_house = np.array([18.0, 20.0, 10.75, 9.50])
your_house = np.array([14.0, 24.0, 14.25, 9.0])

# my_house greater than 18.5 or smaller than 10
print(np.logical_or(my_house > 18.5, my_house < 10))

# Both my_house and your_house smaller than 11
print(np.logical_and(my_house < 11, your_house <11))
```

*IPythonshell*
```
<script.py> output:
    [False  True False  True]
    [False False False  True]
```


1.6 if
---

Conditional statement.
Using if in your coding.
if xxx boolean operators xxx
is True then printxxx
is False then not print
if xx < xx:
   print()
   
Example

*Python script*
```
# Define variables
room = "kit"
area = 14.0

# if statement for room
if room == "kit" :
    print("looking around in the kitchen.")

# if statement for area
if area > 15 :
    print('big place!')
```

*IPythonshell*
```
<script.py> output:
    looking around in the kitchen.
```

1.7 Add else
---
Using else in your coding.
When the first statement 'if' is false it will run your coding below 'else'.

if xxx > xxx:
print()
else
print()

Example

*Python script*
```
# Define variables
room = "kit"
area = 14.0

# if-else construct for room
if room == "kit" :
    print("looking around in the kitchen.")
else :
    print("looking around elsewhere.")

# if-else construct for area
if area > 15 :
    print("big place!")
else :
    print('pretty small.')
```

*IPythonshell*
```
<script.py> output:
    looking around in the kitchen.
    pretty small.
```

1.7 Customize further:elif
---

Using elif in coding.
If first statement 'if' is false,
it will run the second statement 'elif',
and if 'elif' is false it will run the third statement 'else'.

Example

*Python script*
```
# Define variables
room = "bd"
area = 14.0

# if-elif-else construct for room
if room == "kit" :
    print("looking around in the kitchen.")
elif room == "bed":
    print("looking around in the bedroom.")
else :
    print("looking around elsewhere.")

# if-elif-else construct for area
if area > 15 :
    print("big place!")
elif area > 10 :
    print('medium size, nice!')
else :
    print("pretty small.")
```

*IPythonshell*
```
looking around elsewhere.
medium size, nice!
```

1.8 Driving right(1)
---

Using comparison operator in pandas.
Get the boolean colum, then use this to get subset and use subset to get the observation.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Extract drives_right column as Series: dr
dr = cars['drives_right']

# Use dr to subset cars: sel
sel = cars[dr]

# Print sel
print(sel)
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    RU            200         Russia          True
    MOR            70        Morocco          True
    EG             45          Egypt          True
    
```

1.9 Driving right(2)
---

Do this in a simple way, just put the code of dr stright in sel.

Example 

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Convert code to a one-liner
sel = cars[cars['drives_right']]

# Print sel
print(sel)
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    RU            200         Russia          True
    MOR            70        Morocco          True
    EG             45          Egypt          True
```


1.10 Cars per capita(1)
---

Do some execise, that find out the observation that over 500.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Create car_maniac: observations that have a cars_per_cap over 500
car_maniac = cars[cars['cars_per_cap'] >500]



# Print car_maniac
print(car_maniac)
```

*IPythonshell*
```

<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
```



1.11 Cars per capita(2)
---

Use boolean operator on pandas.
np.logical_and()

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Import numpy, you'll need this
import numpy as np

# Create medium: observations with cars_per_cap between 100 and 500
medium = cars[np.logical_and(cars['cars_per_cap'] >= 100,cars['cars_per_cap']<= 500)]
# Print medium
print(medium)
```

*IPythonshell*
```
<script.py> output:
        cars_per_cap country  drives_right
    RU           200  Russia          True
```

