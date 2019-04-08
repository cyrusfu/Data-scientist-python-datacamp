3.Functions and Packages
===

3.1 Familiar Functions
---

Use type() to get the type of varialbe and use print() to print out the type.
Use len() to get the length of varialbe and use print() to print out the length.
Use int() to convert type into integer.

Example

*Python script*

        # Create variables var1 and var2
        var1 = [1, 2, 3, 4]
        var2 = True

        # Print out type of var1
        print(type(var1))

        # Print out length of var1
        print(len(var1))

        # Convert var2 to an integer: out2
        out2 = int(var2)

*IPythonshell*

        <class 'list'>
         4
         

3.2 Multiple Arguments
---

Use help() to know new function.
Use sorted() to sorted your list.
Sorted() takes three arguments iteralbe, key and reverse.
Key = none, means if you dont specify argument key, it will be none.
reverse = False, if you dont specify argument reverse, it will be False. False will sorted your list to upward, True will sorted your list to downward.
Use + to paste those list together.

Example

*Python script*

        # Create lists first and second
        first = [11.25, 18.0, 20.0]
        second = [10.75, 9.50]

        # Paste together first and second: full
        full = first + second

        # Sort full in descending order: full_sorted
        full_sorted = sorted(full,reverse=True)

        # Print out full_sorted
        print(full_sorted)
        
*IPythonshell*

        [20.0, 18.0, 11.25, 10.75, 9.5]
        
Sorted()面对是整个list所以用sorted（list）

3.3 String Methods
---

Use upper() to upper your string.
Use count() to count the number of your variable.

Example:

*Python script*

        # string to experiment with: place
        place = "poolhouse"

        # Use upper() on place: place_up
        place_up = place.upper()

        # Print out place and place_up
        print(place_up)
        print(place)
        # Print out the number of o's in place
        print(place.count('o'))
        
*IPythonshell*

    POOLHOUSE
    poolhouse
    3

3.4 List Methods
---

Use index() to get the index of element.
Use count() to get the time element appears.

Example

*Python script*

        # Create list areas
        areas = [11.25, 18.0, 20.0, 10.75, 9.50]

        # Print out the index of the element 20.0
        print(areas.index(20.0))

        # Print out how often 9.50 appears in areas
        print(areas.count(9.50))

*IPythonshell*

        2
        1
        
3.5 List Methods(2)
---

Use append() to add elements into your list.
Use reverse() to reverse your ordered.

Example

*Python script*

        # Create list areas
        areas = [11.25, 18.0, 20.0, 10.75, 9.50]

        # Use append twice to add poolhouse and garage size
        areas.append(24.5)
        areas.append(15.45)

        # Print out areas
        print(areas)

        # Reverse the orders of the elements in areas
        areas.reverse()

        # Print out areas
        print(areas)

*IPythonshell*

        [11.25, 18.0, 20.0, 10.75, 9.5, 24.5, 15.45]
        [15.45, 24.5, 9.5, 10.75, 20.0, 18.0, 11.25]

3.6 Import package
---

Use import to import package.
To use the method of package.

Example

*Python script*

        # Definition of radius
        r = 0.43

        # Import the math package
        import math

        # Calculate C
        C = 2 * math.pi * r

        # Calculate A
        A = math.pi * r ** 2

        # Build printout
        print("Circumference: " + str(C))
        print("Area: " + str(A))
        
*IPythonshell*

        Circumference: 2.701769682087222
        Area: 0.5808804816487527
        
3.7 Selective Import
---

You can only import one function of package.
from xpackage import xfunction

Example

*Python script*

        # Definition of radius
        r = 192500

        # Import radians function of math package
        from math import radians

        # Travel distance of Moon over 12 degrees. Store in dist.
        dist = r * radians(12)

        # Print out dist
        print(dist)
        
*IPythonshell*

        40317.10572106901
        
