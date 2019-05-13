Dictionaries and Pandas
===

1.1 Motivation for dictionaries
---

Use the traditional way to find the value of someting.
Useing xxx.index() to find the index and store it.
Useing the index just find to get the value.
This is not convenient.

Example

*Python script*

```
# Definition of countries and capital
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']

# Get index of 'germany': ind_ger
ind_ger = countries.index('germany')

# Use ind_ger to print out capital of Germany
print(capitals[ind_ger])
```

*IPythonshell*
```
<script.py> output:
    berlin
```

1.2 Create Dictionaries
---

Create your own dictionaries.
Using dict = {'key':'value'}, print key get value.

Example

*Python script*

```
# Definition of countries and capital
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']

# From string in countries and capitals, create dictionary europe
europe = { 'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Print europe
print(europe)
```

*IPythonshell*

```

<script.py> output:
    {'norway': 'oslo', 'germany': 'berlin', 'spain': 'madrid', 'france': 'paris'}
    
```

1.3 Accese Dictionary
---

Using xxx.keys() to get the keys of your dictionary.
Using xxx.values() to get the values of your dictionary.

Example

*Python script*
```
# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Print out the keys in europe
print(europe.keys())

# Print out value that belongs to key 'norway'
print(europe.values())
```

*IPythonshell*
```
<script.py> output:
    dict_keys(['norway', 'germany', 'spain', 'france'])
    dict_values(['oslo', 'berlin', 'madrid', 'paris'])
```

1.4 Dictionary Manipulation
---

Add value in your dictionary: xxx[]=xxx
To see if xxx in your ditionary: xxx in xxx

Example

*Python script*
```
# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo' }

# Add italy to europe
europe['italy'] = 'rome'

# Print out italy in europe
print('italy' in europe)

# Add poland to europe
europe['poland'] = 'warsaw'

# Print europe
print(europe)
```

*IPythonshell*
```
<script.py> output:
    True
    {'spain': 'madrid', 'poland': 'warsaw', 'italy': 'rome', 'norway': 'oslo', 'germany': 'berlin', 'france': 'paris'}
```

1.5 Dictionary Manipulation(2)
---

Update your dioctionary: xxx[] = xxx
Remove your dictionary: del(xxx[])

Example

*Python script*
```
# Definition of dictionary
europe = {'spain':'madrid', 'france':'paris', 'germany':'bonn',
          'norway':'oslo', 'italy':'rome', 'poland':'warsaw',
          'australia':'vienna' }

# Update capital of germany
europe['germany'] = 'berlin'

# Remove australia
del(europe['australia'])

# Print europe
print(europe)
```

*IPythonshell*
```
<script.py> output:
    {'spain': 'madrid', 'norway': 'oslo', 'italy': 'rome', 'germany': 'berlin', 'france': 'paris', 'poland': 'warsaw'}
```

1.6 Dictionariception
---

Create sub-dictionary.
Add xxx under the key.

Example

*Python script*
```
# Dictionary of dictionaries
europe = { 'spain': { 'capital':'madrid', 'population':46.77 },
           'france': { 'capital':'paris', 'population':66.03 },
           'germany': { 'capital':'berlin', 'population':80.62 },
           'norway': { 'capital':'oslo', 'population':5.084 } }


# Print out the capital of France
print(europe['france'])

# Create sub-dictionary data
data = {'capital':'rome','population':59.83}

# Add data to europe under key 'italy'
europe['italy'] = data

# Print europe
print(europe)
```

*IPythonshell*
```
<script.py> output:
    {'population': 66.03, 'capital': 'paris'}
    {'spain': {'population': 46.77, 'capital': 'madrid'}, 'italy': {'population': 59.83, 'capital': 'rome'}, 'germany': {'population': 80.62, 'capital': 'berlin'}, 'france': {'population': 66.03, 'capital': 'paris'}, 'norway': {'population': 5.084, 'capital': 'oslo'}}
```

1.7 Dictionary to DataFrame(1)
---

Import pandas as pd
Using your dictionary to build a dataframe: pd.dataframe(dict)

Example

*Python script*
```
# Pre-defined lists
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr =  [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]

# Import pandas as pd
import pandas as pd

# Create dictionary my_dict with three key:value pairs: my_dict
my_dict ={'country':names,'drives_right':dr,'cars_per_cap':cpc}

# Build a DataFrame cars from my_dict: cars
cars = pd.DataFrame(my_dict)

# Print cars
print(cars)
```

*IPythonshell*
```
<script.py> output:
       cars_per_cap        country  drives_right
    0           809  United States          True
    1           731      Australia         False
    2           588          Japan         False
    3            18          India         False
    4           200         Russia          True
    5            70        Morocco          True
    6            45          Egypt          True
```

1.8 Dictionary to Dataframe(2)
---

Change the row labels of your dataframe: xxx.index = []

Example

*Python script*
```
import pandas as pd

# Build cars DataFrame
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr =  [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]
dict = { 'country':names, 'drives_right':dr, 'cars_per_cap':cpc }
cars = pd.DataFrame(dict)
print(cars)

# Definition of row_labels
row_labels = ['US', 'AUS', 'JAP', 'IN', 'RU', 'MOR', 'EG']

# Specify row labels of cars
cars.index = row_labels

# Print cars again
print(cars)
```

*IPythonshell*
```
<script.py> output:
       cars_per_cap        country  drives_right
    0           809  United States          True
    1           731      Australia         False
    2           588          Japan         False
    3            18          India         False
    4           200         Russia          True
    5            70        Morocco          True
    6            45          Egypt          True
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
    IN             18          India         False
    RU            200         Russia          True
    MOR            70        Morocco          True
    EG             45          Egypt          True
```

1.9 CSV to Dataframe(1)
---

How to import csv file and store it.

Example

*Python script*
```
# Import pandas as pd
import pandas as pd

# Import the cars.csv data: cars
cars = pd.read_csv('cars.csv')

# Print out cars
print(cars)
```

*IPythonshell*
```
<script.py> output:
      Unnamed: 0  cars_per_cap        country  drives_right
    0         US           809  United States          True
    1        AUS           731      Australia         False
    2        JAP           588          Japan         False
    3         IN            18          India         False
    4         RU           200         Russia          True
    5        MOR            70        Morocco          True
    6         EG            45          Egypt          True

```

1.10 CSV to Datafrme(2)

Fix the index col: pd.read_csv('',index_col = 0)

Example

*Python script*
```
# Import pandas as pd
import pandas as pd

# Fix import by including index_col
cars = pd.read_csv('cars.csv',index_col = 0)

# Print out cars
print(cars)
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
    IN             18          India         False
    RU            200         Russia          True
    MOR            70        Morocco          True
    EG             45          Egypt          True
```

We can see the the index colum changed.

1.11 Square Brackets(1)
---

To print the column you want in pandas serise and pandas dataframe.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
print(cars)
# Print out country column as Pandas Series
print(cars['country'])

# Print out country column as Pandas DataFrame
print(cars[['country']])

# Print out DataFrame with country and drives_right columns
print(cars[['country','drives_right']])
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
    IN             18          India         False
    RU            200         Russia          True
    MOR            70        Morocco          True
    EG             45          Egypt          True
    US     United States
    AUS        Australia
    JAP            Japan
    IN             India
    RU            Russia
    MOR          Morocco
    EG             Egypt
    Name: country, dtype: object
               country
    US   United States
    AUS      Australia
    JAP          Japan
    IN           India
    RU          Russia
    MOR        Morocco
    EG           Egypt
               country  drives_right
    US   United States          True
    AUS      Australia         False
    JAP          Japan         False
    IN           India         False
    RU          Russia          True
    MOR        Morocco          True
    EG           Egypt          True

```

1.12 Square Brackets(2)
---

Using square brackets to get rows.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out first 3 observations
print(cars[0:3])

# Print out fourth, fifth and sixth observation
print(cars[3:6])
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
        cars_per_cap country  drives_right
    IN            18   India         False
    RU           200  Russia          True

<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
         cars_per_cap  country  drives_right
    IN             18    India         False
    RU            200   Russia          True
    MOR            70  Morocco          True

```

1.13 loc and iloc(1)
---

Using loc and iloc to print the rows you want.
When you deal with two rows(loc) only use [[]].


Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)
print(cars)
# Print out observation for Japan
print(cars.loc['JAP'])

# Print out observations for Australia and Egypt
print(cars.loc[['AUS','EG']])
```

*IPythonshell*
```
<script.py> output:
         cars_per_cap        country  drives_right
    US            809  United States          True
    AUS           731      Australia         False
    JAP           588          Japan         False
    IN             18          India         False
    RU            200         Russia          True
    MOR            70        Morocco          True
    EG             45          Egypt          True
    cars_per_cap      588
    country         Japan
    drives_right    False
    Name: JAP, dtype: object
         cars_per_cap    country  drives_right
    AUS           731  Australia         False
    EG             45      Egypt          True

```

1.14 loc and iloc(2)
---

Using loc and iloc to select both row and colum
Using loc and iloc to select mutiple rows and colums

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out drives_right value of Morocco
print(cars.loc[['MOR','drives_right']])

# Print sub-DataFrame
print(cars.loc[['RU','MOR'],['country','drives_right']])
```

*IPythonshell*
```
      cars_per_cap  country drives_right
MOR                   70.0  Morocco         True
drives_right           NaN      NaN          NaN

<script.py> output:
                  cars_per_cap  country drives_right
    MOR                   70.0  Morocco         True
    drives_right           NaN      NaN          NaN
         country  drives_right
    RU    Russia          True
    MOR  Morocco          True

```

1.15 loc and iloc(3)
---

Using loc and iloc to print colums in series and dataframe.

Example

*Python script*
```
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col = 0)

# Print out drives_right column as Series
print(cars.loc[:,'drives_right'])

# Print out drives_right column as DataFrame
print(cars.loc[:,['drives_right']])

# Print out cars_per_cap and drives_right as DataFrame
print(cars.loc[:,['cars_per_cap','drives_right']])
```

*IPythonshell*
<script.py> output:
    US      True
    AUS    False
    JAP    False
    IN     False
    RU      True
    MOR     True
    EG      True
    Name: drives_right, dtype: bool
         drives_right
    US           True
    AUS         False
    JAP         False
    IN          False
    RU           True
    MOR          True
    EG           True
         cars_per_cap  drives_right
    US            809          True
    AUS           731         False
    JAP           588         False
    IN             18         False
    RU            200          True
    MOR            70          True
    EG             45          True

```
