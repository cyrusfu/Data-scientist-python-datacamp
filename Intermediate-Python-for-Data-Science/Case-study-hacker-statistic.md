Case Study Hacker Statisics
===

1.Random Float
---

There is a random package in numpy package.

Import numpy as np and to get random package.

You can selecet seed() to produce the same result.

Use rand to chose a random float from 0 to 1.

*Python script*
```
# Import numpy as np
import numpy as np

# Set the seed
np.random.seed(123)

# Generate and print random float
print(np.random.rand())
```

*IPythonshell*
```
0.6964691855978616
```

2.Roll the dice
---

Also you can use randint to generates a random integer.

*Python script*
```
# Import numpy and set seed
import numpy as np
np.random.seed(123)

# Use randint() to simulate a dice
print(np.random.randint(1,7))

# Use randint() again
print(np.random.randint(1,7))
```

*IPythonshell*
```
3
```

1.3.Determine your next move
---

Use if loop and randint to simulate dice.

*Python script*
```
# Numpy is imported, seed is set

# Starting step
step = 50

# Roll the dice
dice = np.random.randint(1,7)

# Finish the control construct
if dice <= 2 :
    step = step - 1
elif 3 <= dice <= 5:
    step = step + 1
else :
    step = step + np.random.randint(1,7)

# Print out dice and step
print(dice)
print(step)
```
*IPythonshell*
```
  6
  53
```

4.
