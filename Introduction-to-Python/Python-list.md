2.Python List
===

2.1 Create a list & 2.2 Create list with differet types
---

List is a **compound data type**.
List can mix different type of varialbe together.
Use [] and , to create a list.

Example

*Python script:

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

*IPythonshell:

    [11.25, 18.0, 20.0, 10.75, 9.5, 'ar', True, 10]

Other example

*Python script:

    # area variables (in square meters)
    hall = 11.25
    kit = 18.0
    liv = 20.0
    bed = 10.75
    bath = 9.50

    # Adapt list areas
    areas = ["hallway", hall, "kitchen", kit, "living room", liv, "bedroom", bed, "bathroom", bath]

    # Print areas

*IPythonshell:

    <script.py> output:
        ['hallway', 11.25, 'kitchen', 18.0, 'living room', 20.0, 'bedroom', 10.75, 'bathroom', 9.5]
    
    
**Conclusion: As we see before this list mix int, float, string and event boolean together, and we can use [] to create list, , to seperat those varialbes.**


2.3 List of lists
---

Instead of put strings and int olny in a list, you can create a list of list to give a better view.
Use [[,],[,]] to build a list of list.

Example

*Python script:

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
    
*IPythonshell:

    [['hallway', 11.25], ['kitchen', 18.0], ['living room', 20.0], ['bedroom', 10.75], ['bathroom', 9.5]]
    <class 'list'>
    

