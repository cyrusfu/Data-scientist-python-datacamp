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
