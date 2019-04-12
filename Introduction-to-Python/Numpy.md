4.Numpy
===

4.1 Your First Numpy Array
---

Introduction about Numpy package.
Learn to import numpy and to convert list into numpy array.


Example

*Python script*

        # Create list baseball
        baseball = [180, 215, 210, 210, 188, 176, 209, 200]

        # Import the numpy package as np
        import numpy as np

        # Create a numpy array from baseball: np_baseball
        np_baseball = np.array(baseball)

        # Print out type of np_baseball
        print(type(np_baseball))
        
*IPythonshell*

        <class 'numpy.ndarray'>
        
4.2 Use Numpy Array
---

Create a numpy array and use your array to do some calculation.

Example

*Python script*

        # height is available as a regular list

        # Import numpy
        import numpy as np

        # Create a numpy array from height_in: np_height_in
        np_height_in = np.array(height_in)

        # Print out np_height_in
        print(np_height_in)

        # Convert np_height_in to m: np_height_m
        np_height_m = np_height_in * 0.0254

        # Print np_height_m
        print(np_height_m)
        
*IPythonshell*

        <script.py> output:
                [74 74 72 ..., 75 75 73]
                [ 1.8796  1.8796  1.8288 ...,  1.905   1.905   1.8542]
                
4.3 Numpy array (3)
---

Use numpy array to select the elements.

Example

*Python script*

        # height and weight are available as a regular lists

        # Import numpy
        import numpy as np

        # Calculate the BMI: bmi
        np_height_m = np.array(height_in) * 0.0254
        np_weight_kg = np.array(weight_lb) * 0.453592
        bmi = np_weight_kg / np_height_m ** 2

        # Create the light array
        light = bmi < 21

        # Print out light
        print(light)
        
        # Print out BMIs of all baseball players whose BMI is below 21
        print(bmi[light]) #use [] for list.

*IPythonshell*

        <script.py> output:
        [False False False ..., False False False]
        [ 20.54255679  20.54255679  20.69282047  20.69282047  20.34343189
        20.34343189  20.69282047  20.15883472  19.4984471   20.69282047
        20.9205219 ]
        

        # Print out BMIs of all baseball players whose BMI is below 21
        print(bmi[light])
        

4.4 Subsetting Numpy Array

Use index to select elements from numpy array.

Example

*Python script*


        # height and weight are available as a regular lists

        # Import numpy
        import numpy as np

        # Store weight and height lists as numpy arrays
        np_weight_lb = np.array(weight_lb)
        np_height_in = np.array(height_in)

        # Print out the weight at index 50
        print(weight_lb[50])

        # Print out sub-array of np_height_in: index 100 up to and including index 110
        print(np_height_in[100:111])
        
*IPythonshell*

        <script.py> output:
                200
                [73 74 72 73 69 72 73 75 75 73 72]
                
4.5 Your First 2D Numpy Array
---

Use a list of list to creat your first 2D Numpy Array.

Example

*Python script*

```
# Create baseball, a list of lists
baseball = [[180, 78.4],
            [215, 102.7],
            [210, 98.5],
            [188, 75.2]]

# Import numpy
import numpy as np

# Create a 2D numpy array from baseball: np_baseball
np_baseball = np.array(baseball)

# Print out the type of np_baseball
print(type(np_baseball))

# Print out the shape of np_baseball
print(np_baseball.shape)    
```

*IPythonshell*

```
 output:
    
    (4, 2)
```

4.6 Subsetting 2D Numpy Arrays
---

Use numpy arrays to build your 2d numpy arrays.
Use [,] to select the row or column you want.

Example

*Python scirpt*

        # baseball is available as a regular list of lists

        # Import numpy package
        import numpy as np

        # Create np_baseball (2 cols)
        np_baseball = np.array(baseball)

        # Print out the 50th row of np_baseball
        print(np_baseball[49,:])

        # Select the entire second column of np_baseball: np_weight_lb
        np_weight_lb = np_baseball[:,1]

        # Print out height of 124th player
        print(np_baseball[123,0])
        
*IPythonshell*

        <script.py> output:
         [ 70 195]
         75
         
4.7 2D Arithmetic
---

To calculate the addition of numpy arrays.
To calculate the product of numpy arrays.

Example

*Python script*

        # baseball is available as a regular list of lists
        # updated is available as 2D numpy array

        # Import numpy package
        import numpy as np

        # Create np_baseball (3 cols)
        np_baseball = np.array(baseball)

        # Print out addition of np_baseball and updated
        print(np_baseball + updated)

        # Create numpy array: conversion
        conversion = np.array([0.0254,0.453592,1])

        # Print out product of np_baseball and conversion
        print(np_baseball * conversion)

*IPythonshell*

        [[  75.2303559   168.83775102   23.99      ]
         [  75.02614252  231.09732309   35.69      ]
         [  73.1544228   215.08167641   31.78      ]
        ..., 
        [  76.09349925  209.23890778   26.19      ]
        [  75.82285669  172.21799965   32.01      ]
        [  73.99484223  203.14402711   28.92      ]]
        [[  1.8796   81.64656  22.99   ]
         [  1.8796   97.52228  34.69   ]
         [  1.8288   95.25432  30.78   ]
        ..., 
        [  1.905    92.98636  25.19   ]
        [  1.905    86.18248  31.01   ]
        [  1.8542   88.45044  27.92   ]]
        
4.8 Average versus Median
---

Use the numpy package's function np.mean() and np.median() to calculate the mean and median.

Example 

*Python script*

        # np_baseball is available

        # Import numpy
        import numpy as np

        # Create np_height_in from np_baseball
        np_height_in = np_baseball[:,0]

        # Print out the mean of np_height_in
        print(np.mean(np_height_in))

        # Print out the median of np_height_in
        print(np.median(np_height_in))
        
*IPythonshell*

        <script.py> output:
        1586.46108374
        74.0
        
4.9 Explore Numpy
---

Use numpy package to calculate the standard deviation and correlation.

Example

*Python script*

```
# np_baseball is available

# Import numpy
import numpy as np

# Print mean height (first column)
avg = np.mean(np_baseball[:,0])
print("Average: " + str(avg))

# Print median height. Replace 'None'
med = np.median(np_baseball[:,0])
print("Median: " + str(med))

# Print out the standard deviation on height. Replace 'None'
stddev = np.std(np_baseball[:,0])
print("Standard Deviation: " + str(stddev))

# Print out correlation between first and second column. Replace 'None'
corr = np.corrcoef(np_baseball[:,0],np_baseball[:,1])
print("Correlation: " + str(corr))
```

*IPythonshell*

```
<script.py> output:
    Average: 73.6896551724
    Median: 74.0
    Standard Deviation: 2.31279188105
    Correlation: [[ 1.          0.53153932]
     [ 0.53153932  1.        ]]
```

4.10 Summary

Build numpy array.
Select an specify elements from numpy array.
calculate the median.
Use xxx == 'xxx' to get the bool.
xxxx[xxx == 'xxx' ] to get the specify elements.( if it is True then it will be selected, if it is a false then it won't be selected)

Example

*Python script*
```
# heights and positions are available as lists

# Import numpy
import numpy as np

# Convert positions and heights to numpy arrays: np_positions, np_heights
np_postions = np.array(positions)
np_heights = np.array(heights)

# Heights of the goalkeepers: gk_heights
gk_heights = np_heights[np_postions == 'GK']

# Heights of the other players: other_heights
other_heights = np_heights[np_postions != 'GK']

# Print out the median height of goalkeepers. Replace 'None'
print("Median height of goalkeepers: " + str(np.median(gk_heights)))

# Print out the median height of other players. Replace 'None'
print("Median height of other players: " + str(np.median(other_heights)))
print(np_postions == 'GK')
```

*IPythonshell*
```
Median height of goalkeepers: 188.0
Median height of other players: 181.0
[ True False False ..., False False False]
```
