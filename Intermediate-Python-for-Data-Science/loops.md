Loops
===

1.1 Basic While Loops
---

While loop will keep running as long as the statement is correct.
So we can set a inverted pendulum to control it.
Practice with while loop.

Example

*Python script*
```
#set a offset
offset = 8

#set a while loop with offset

While offset != 0 :
   print('correcting...')
   offset = offset - 1
   print(offset)
```

*IPythonshell*
```
<script.py> output:
    correcting...
    7
    correcting...
    6
    correcting...
    5
    correcting...
    4
    correcting...
    3
    correcting...
    2
    correcting...
    1
    correcting...
    0
```

1.2 Add Conditionals
---

Sometimes you will meet some problem that your while loop will keep run forever.
So you need add some conditionals to make sure it works.

Example

*Python script*
```
# Initialize offset
offset = -6

# Code the while loop
while offset != 0 :
    print("correcting...")
    if offset > 0:
        offset = offset - 1
    else :
        offset = offset + 1
    print(offset)
```

*IPythonshell*
```
<script.py> output:
    correcting...
    -5
    correcting...
    -4
    correcting...
    -3
    correcting...
    -2
    correcting...
    -1
    correcting...
    0
```

1.3 Loop over a list
---

Use for loop to print every element separately.

Example

*Python script*
```
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Code the for loop
for rooms in areas :
    print(rooms)
```

*IPythonshell*
```
<script.py> output:
    11.25
    18.0
    20.0
    10.75
    9.5
```

1.4 Indexes and Values
---

If you  want to access every element separately and also the index information
Use enumerate() 

for index, x in enumerate(xx)

Example

*Python script*
```
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Change for loop to use enumerate() and update print()
for index,a in enumerate(areas) :
    print('room' + str(index) + ':' + str(a))
```

*IPythonshell*
```
<script.py> output:
    room0:11.25
    room1:18.0
    room2:20.0
    room3:10.75
    room4:9.5
```
You can also add 1 in index so that the first will be room1:11.25

1.5 Loop over list of lists
---

Build a loop for list of lists.
Use for x in xx:
    print()
    
Example

*Python script*
```
# house list of lists
house = [["hallway", 11.25], 
         ["kitchen", 18.0], 
         ["living room", 20.0], 
         ["bedroom", 10.75], 
         ["bathroom", 9.50]]
         
# Build a for loop from scratch
for a in house :
    print('the ' + str(a[0]) + ' is ' + str(a[1]) +' sqm')
```

*IPythonshell*
```
<script.py> output:
    the hallway is 11.25 sqm
    the kitchen is 18.0 sqm
    the living room is 20.0 sqm
    the bedroom is 10.75 sqm
    the bathroom is 9.5 sqm
```

1.6 Loop over dictionary
---

Use for key, values in xxx.items():
    print(key + str(values))
Can get the key and values from dictionary by for loop.

Example

*Python script*
```
# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin',
          'norway':'oslo', 'italy':'rome', 'poland':'warsaw', 'austria':'vienna' }
          
# Iterate over europe
for key, values in europe.items() :
    print('the capital of ' + key + ' is ' +str(values) )
```

*IPythonshell*
```
<script.py> output:
    the capital of spain is madrid
    the capital of france is paris
    the capital of italy is rome
    the capital of poland is warsaw
    the capital of austria is vienna
    the capital of germany is berlin
    the capital of norway is oslo
```

1.7 Loop over numpy array
---

Use for loop to get element of 1d numpy array and 2d numpy array.
Use for xxx in np_xxx:
   print()
To get the elements of 1d numpy array.

Use for xxx in np.nditer():
   print()
To deal with 2d numpy array.

Example

*Python script*
```
# Import numpy as np
import numpy as np

# For loop over np_height
for height in np_height :
    print(str(height) + ' inches')

# For loop over np_baseball
for bb in np.nditer(np_baseball) : 
    print(bb)
```

*IPythonshell*
```
<script.py> output:
    74 inches
    74 inches
    72 inches
    72 inches
    73 inches
    69 inches
    
    69
    71
    76
    72
    72
    70
    240
    150
    200
    215
    202
    200
```


1.8 Loop over DataFrame(1)
---

Use for loop to print lab and rows of dataframe.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Iterate over rows of cars
for lab, rows in cars.iterrows() :
    print(lab)
    print(rows)
```

*IPythonshell*
```
US
    cars_per_cap              809
    country         United States
    drives_right             True
    Name: US, dtype: object
    AUS
    cars_per_cap          731
    country         Australia
    drives_right        False
    Name: AUS, dtype: object
    JAP
    cars_per_cap      588
    country         Japan
    drives_right    False
    Name: JAP, dtype: object
    IN
    cars_per_cap       18
    country         India
    drives_right    False
    Name: IN, dtype: object
    RU
    cars_per_cap       200
    country         Russia
    drives_right      True
    Name: RU, dtype: object
    MOR
    cars_per_cap         70
    country         Morocco
    drives_right       True
    Name: MOR, dtype: object
    EG
    cars_per_cap       45
    country         Egypt
    drives_right     True
    Name: EG, dtype: object
```

1.9 Loop over DataFrame(2):
---

Print the lab and row.
Select the values you want from dataframe.
use
for lab, row in cars.iterrows() :
    print(lab + '' + str(row['xxx']
    
Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Adapt for loop
for lab, row in cars.iterrows() :
    print(lab + ": " +str(row['cars_per_cap']))
```

*IPythonshell*
```
<script.py> output:
    US: 809
    AUS: 731
    JAP: 588
    IN: 18
    RU: 200
    MOR: 70
    EG: 45
```

1.10 Add column(1)
---

Use for loop to add column in dataframe.
for lab, row in xxx.iterrows() :
    xxx.loc['xx'] = len(row[''])
    
Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Code for loop that adds COUNTRY column
for lab, row in cars.iterrows() :
    cars.loc[lab,'COUNTRY'] = row['country'].upper()


# Print cars
print(cars)
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right        COUNTRY
    US            809  United States          True  UNITED STATES
    AUS           731      Australia         False      AUSTRALIA
    JAP           588          Japan         False          JAPAN
    IN             18          India         False          INDIA
    RU            200         Russia          True         RUSSIA
    MOR            70        Morocco          True        MOROCCO
    EG             45          Egypt          True          EGYPT
```

1.11 Add colum(2)
---

For more efficient.
Use apply to add column in dataframe.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Use .apply(str.upper)
cars['COUNTRY'] = cars['country'].apply(str.upper)
```

*IPythonshell*
```
 cars_per_cap        country  drives_right        COUNTRY
US            809  United States          True  UNITED STATES
AUS           731      Australia         False      AUSTRALIA
JAP           588          Japan         False          JAPAN
IN             18          India         False          INDIA
RU            200         Russia          True         RUSSIA
MOR            70        Morocco          True        MOROCCO
EG             45          Egypt          True          EGYPT
```
