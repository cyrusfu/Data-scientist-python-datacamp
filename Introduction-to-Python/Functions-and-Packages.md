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



       
