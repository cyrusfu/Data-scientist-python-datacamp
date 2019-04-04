[toc]
2.Python List
===

2.1 Create a list & 2.2 Create list with differet types
---

List is a **compound data type**.
List can mix different type of varialbe together.
Use [] and , to create a list.

Example

*Python script:*

    # area variables (in square meters)
    hall = 11.25
    kit = 18.0
    liv = 20.0
    bed = 10.75
    bath = 9.50
    
    # Create list areas
    areas = [hall, kit, liv, bed, bath, 'ar', True, 10]

    # Print areas
    print(areas)

*IPythonshell:*

    [11.25, 18.0, 20.0, 10.75, 9.5, 'ar', True, 10]

Other example

*Python script:*

    # area variables (in square meters)
    hall = 11.25
    kit = 18.0
    liv = 20.0
    bed = 10.75
    bath = 9.50

    # Adapt list areas
    areas = ["hallway", hall, "kitchen", kit, "living room", liv, "bedroom", bed, "bathroom", bath]

    # Print areas

*IPythonshell:*

    <script.py> output:
        ['hallway', 11.25, 'kitchen', 18.0, 'living room', 20.0, 'bedroom', 10.75, 'bathroom', 9.5]
    
    
**Conclusion: As we see before this list mix int, float, string and event boolean together, and we can use [] to create list, , to seperat those varialbes.**


2.3 List of lists
---

Instead of put strings and int olny in a list, you can create a list of list to give a better view.
Use [[,],[,]] to build a list of list.

Example

*Python script:*

    # area variables (in square meters)
    hall = 11.25
    kit = 18.0
    liv = 20.0
    bed = 10.75
    bath = 9.50

    # house information as list of lists
    house = [['hallway', hall], ['kitchen', kit], ['living room', liv], ['bedroom', bed], ['bathroom', bath]]
    
    # Print out house
    print(house)

    # Print out the type of house
    print(type(house))
    
*IPythonshell:*

    [['hallway', 11.25], ['kitchen', 18.0], ['living room', 20.0], ['bedroom', 10.75], ['bathroom', 9.5]]
    <class 'list'>
    

2.4 Subset and conquer
---

**Use [1] to select the second element of your list.
Also can use [-1] to select the last element of your list.**

Example

*Python script*

    # Create the areas list
    areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

    # Print out second element from areas
    print(areas[1])

    # Print out last element from areas
    print(areas[-1])

    # Print out the area of the living room
    print(areas[5])

*IPythonshell*

    <script.py> output:
        11.25
        9.5
        20.0
        
**Python counting the element of list start from 0.
eg.
-5,-4,-3,-2,-1**

**[a,s,d,f,g]**

**0,1,2,3,4**

2.5 Subset and calculate
---

Use subset of your list to do the calculation.

Example
you have a list of your house, and you want to know the areas of kitchen and bedroom.

*Python script*

    # Create the areas list
    areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

    # Sum of kitchen and bedroom area: eat_sleep_area
    eat_sleep_area = areas[3] + areas[-3]

    # Print the variable eat_sleep_area
    print(eat_sleep_area)
    
*IPythonshell:*

    <script.py> output:
        28.75


2.6 Slicing and dicing
---

Selecting single values from a list is just one part of the story. It's also possible to slice your list, which means selecting multiple elements from your list. 

**Use the following syntax:**

    my_list[start:end]
**The start index will be included, while the end index is not.**

Example

*Python script*

    # Create the areas list
    areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

    # Use slicing to create a list, downstairs, that contains the first 6 elements of areas.
    downstairs = areas[0:6]

    # Do a similar thing to create a new variable, upstairs, that contains the last 4 elements of areas.
    upstairs = areas[6:10]

    # Print out downstairs and upstairs
    print(downstairs)
    print(upstairs)
    
    
*IPythonshell*

    <script.py> output:
        ['hallway', 11.25, 'kitchen', 18.0, 'living room', 20.0]
        ['bedroom', 10.75, 'bathroom', 9.5]
        
**You can not use [-1,-2] to slicing the list.**

**If you don't specify the begin index, Python figures out that you want to start your slice at the beginning of your list. If you don't specify the end index, the slice will go all the way to the last element of your list.**

Example 

*Python script*

    # Create the areas list
    areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

    # Alternative slicing to create downstairs. The first 6 elements of areas.
    downstairs = areas[:6]

    # Alternative slicing to create upstairs. The last 4 elements of areas
    upstairs = areas[6:]
    
    print(downstairs)
    print(upstairs)
    
*IPythonshell*

    ['hallway', 11.25, 'kitchen', 18.0, 'living room', 20.0]
    ['bedroom', 10.75, 'bathroom', 9.5]
    
    
2.7 Replace list elements
---

Simply subset the list and assign new values to the subset. You can select single elements or you can change entire list slices at once.

Example

*Python script*

    # Create the areas list
    areas = ["hallway", 11.25, "kitchen", 18.0, "living room", 20.0, "bedroom", 10.75, "bathroom", 9.50]

    # Correct the bathroom area to 10.50 instead of 9.50
    areas[-1] = 10.50

    # Change "living room" to "chill zone"

    areas[4] = 'chill zone'

    print(areas)

*IPythonshell*

    ['hallway', 11.25, 'kitchen', 18.0, 'chill zone', 20.0, 'bedroom', 10.75, 'bathroom', 10.5]
    
    
2.8 Extend a list
---

How to extend your list?
Use '+' to add element to your list.

Example

*Python script*

    # Create the areas list and make some changes
    areas = ["hallway", 11.25, "kitchen", 18.0, "chill zone", 20.0,
            "bedroom", 10.75, "bathroom", 10.50]

    # Add poolhouse data to areas, new list is areas_1
    areas_1 = areas + ['poolhouse', 24.5]

    # Add garage data to areas_1, new list is areas_2

    areas_2 = areas_1 + ['garage', 15.45]

    print(areas_2)

*IPythonshell*

    ['hallway', 11.25, 'kitchen', 18.0, 'chill zone', 20.0, 'bedroom', 10.75, 'bathroom', 10.5, 'poolhouse', 24.5, 'garage', 15.45]

2.9 Delete list elements
---

Use del() statement to remove elements of your list.

Example

*Python script*

    In [5]:  x = ["a", "b", "c", "d"]
    ... ... del(x[1])
    ... ... x
*IPythonshell*

    Out[6]: ['a', 'c', 'd']

**Use del() and select the elemets that you want to deleta by using x[].
Otherwise you can use x[,] to deleta multiple elememts of your list.**

**The ; sign is used to place commands on the same line. The following two code chunks are equivalent:**

    # Same line
    command1; command2

    # Separate lines
    command1
    command2
    
Example

*Python script*

    #delet the poolhouse and the areas data from list
    areas = ["hallway", 11.25, "kitchen", 18.0,
            "chill zone", 20.0, "bedroom", 10.75,
            "bathroom", 10.50, "poolhouse", 24.5,
            "garage", 15.45]
    del(areas[-4:-2]); print(areas)

*IPythonshell*

    areas = ["hallway", 11.25, "kitchen", 18.0,
             "chill zone", 20.0, "bedroom", 10.75,
             "bathroom", 10.50,"garage", 15.45]


