1.Matplotlib
===
In this charpter we will learn how to virsulized and structured your data by using Matplotlib.

1.1 Line plot(1)
---

Import matplotlib as plt.
Use plt.plot(x,y) to build your line plot.

Example

*Python script*
```
# Print the last item from year and pop
print(year[-1])
print(pop[-1])

# Import matplotlib.pyplot as plt
import matplotlib.pyplot as plt

# Make a line plot: year on the x-axis, pop on the y-axis
plt.plot(year,pop)

# Display the plot with plt.show()
plt.show()
```

*IPythonshell*
```
<script.py> output:
    2100
    10.85
```
![avatar](https://thumbnail0.baidupcs.com/thumbnail/52ff4f03db36bd0b7ba1372705dd6f7f?fid=3730888783-250528-810682798080087&time=1555056000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-1X35tXFNlU51WY0p35j7mwQd25U%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2358779941931119917&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)


1.2 Line plot(2)
---

Use plt.plot to build a line plot.
Use plt.show() to show the plot.

Example 

*Python script*
```
# Print the last item of gdp_cap and life_exp
print(gdp_cap[-1])
print(life_exp[-1])

# Make a line plot, gdp_cap on the x-axis, life_exp on the y-axis
plt.plot(gdp_cap,life_exp)

# Display the plot
plt.show()
```

*IPythonshell*
```
<script.py> output:
    469.70929810000007
    43.487
```
![avatar](https://thumbnail0.baidupcs.com/thumbnail/f286a2ee8abbf3fded76937cc3a40b2e?fid=3730888783-250528-929140149197988&time=1555056000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-zeGhiB0g5xPdpZlF9blTCOSKPrQ%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2358847365947123499&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

1.3 Scatter Plot
---

Use plt.scatter() tu build a scatterplot.
For a better view, use plt.xscale() to give the better scale for a better view.

Example

a.If you do not change the xscale

*Python script*
```
# Change the line plot below to a scatter plot
plt.scatter(gdp_cap, life_exp)

# Put the x-axis on a logarithmic scale

# Show plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/f41f0439c3f0378d8f4310b3dc16ab2c?fid=3730888783-250528-312668319005379&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-seVZeQMWJeAyaafSj06az36VxH0%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2358965791052885975&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

b.If you change the x-scale

*Python script*
```
# Change the line plot below to a scatter plot
plt.scatter(gdp_cap, life_exp)

# Put the x-axis on a logarithmic scale
plt.xscale('log')

# Show plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4cfdc5ec2a29b9d666d3b42a8b30f055?fid=3730888783-250528-1013308925970959&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-3WI6kkbbD73vw9i2QRD7vMQQmTQ%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2358988343900205191&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

Remember use plt.xscale() to make a better view.


1.4 Scatter plot(2)
---

Import matplotlib pakage.
Build scatter plot.
Show the plot.

Example

*Python script*
```
# Import package
import matplotlib.pyplot as plt

# Build Scatter plot
plt.scatter(pop,life_exp)

# Show plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4cfdc5ec2a29b9d666d3b42a8b30f055?fid=3730888783-250528-1013308925970959&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-3WI6kkbbD73vw9i2QRD7vMQQmTQ%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359057980934801264&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)


1.5 Build a Histogram
---

Use plt.hist() to build the histogram.
Use plt.show() to show the graphy.

*Python script*
```
# Create histogram of life_exp data
plt.hist(life_exp)

# Display histogram
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/6328fbc25a4b1138e868772edaa374b4?fid=3730888783-250528-281165338367391&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-fScFS8aAUPd9iY1NBS5sysMGa%2FE%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359182222224099652&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

1.6 Build a histogram(2): Bins
---

Use plt.hist(xxx,bins = x) to chose the number of bins you want in histogram.
Use plt.clf() to clean the last pic otherwise it will combined.
Use plt.show() to show the graphy.

Example

a. if you do not use plt.clf() to clean the last pic.

*Python script*
```
# Build histogram with 5 bins
plt.hist(life_exp, bins = 5)

# Show and clean up plot
plt.show()


# Build histogram with 20 bins
plt.hist(life_exp, bins = 20)

# Show and clean up again
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4d07dd2414ebe6b8cd07c78836c1c6d2?fid=3730888783-250528-275116827184735&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-PmA7z5FwdRY1JTMAX5Nj%2BqtlHqo%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359287451383994724&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

![avatar](https://thumbnail0.baidupcs.com/thumbnail/2a20e92ad2c29815ea51a171452028cb?fid=3730888783-250528-222187959145345&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-SY1laNpUJlT0n1YcvOrIfWGGO1Q%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359320513403493981&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

b.if you use plt.clf to clean the last picture.

*Python script*
```
# Build histogram with 5 bins
plt.hist(life_exp, bins = 5)

# Show and clean up plot
plt.show()
plt.clf()

# Build histogram with 20 bins
plt.hist(life_exp, bins = 20)

# Show and clean up again
plt.show()
plt.clf()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4d07dd2414ebe6b8cd07c78836c1c6d2?fid=3730888783-250528-275116827184735&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-PmA7z5FwdRY1JTMAX5Nj%2BqtlHqo%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359287451383994724&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

![avatar](https://thumbnail0.baidupcs.com/thumbnail/d6d867be56df44e89583c18ecaec92a0?fid=3730888783-250528-639985530350509&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-eIsTGHORsULhdxNOC%2FizkdTFyyw%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359298981216199442&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)


1.7 Build a Histogram(3): compare
---

Compare two histogram.

Example

*Python script*

```
# Histogram of life_exp, 15 bins
plt.hist(life_exp, bins = 15)

# Show and clear plot
plt.show()
plt.clf()

# Histogram of life_exp1950, 15 bins
plt.hist(life_exp1950, bins = 15)

# Show and clear plot again
plt.show()
plt.clf()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/8e835a0c02c47ff25fafcc7ec0e2e74d?fid=3730888783-250528-30828358752049&time=1555398000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-b7OD%2FXhpGD2GVQm2yAGPujtojBM%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2450360952121763392&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

![avatar](https://thumbnail0.baidupcs.com/thumbnail/b7843cbe66c308760da685037b458967?fid=3730888783-250528-151499422098719&time=1555398000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-dLdgjCuCdpXnIHVmXb7gm1zbYfs%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2450354874203702759&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)


1.8 Labels
---

Learning how to add labels to your x-axis and y-axis
Learning how to add title to your graphy.
plt.xlabel()
plt.ylabel()
plt.title()


*Python script*

```
# Basic scatter plot, log scale
plt.scatter(gdp_cap, life_exp)
plt.xscale('log') 

# Strings
xlab = 'GDP per Capita [in USD]'
ylab = 'Life Expectancy [in years]'
title = 'World Development in 2007'

# Add axis labels
plt.xlabel(xlab)
plt.ylabel(ylab)

# Add title
plt.title(title)

# After customizing, display the plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/b65544cce2b75d1e7145338efa15b83f?fid=3730888783-250528-1063165570148493&time=1555398000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-conoALmOlmIsN31%2FK8B%2FZYfiq5o%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2450579393852887760&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

1.9 Ticks
---

Using plt.xticks(x1,x2) to change the x-ticks
Using plt.yticks(y1,y2) to change the y-ticks

Example

*Python script*

```
# Scatter plot
plt.scatter(gdp_cap, life_exp)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')

# Definition of tick_val and tick_lab
tick_val = [1000, 10000, 100000]
tick_lab = ['1k', '10k', '100k']

# Adapt the ticks on the x-axis
plt.xticks(tick_val,tick_lab)

# After customizing, display the plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/aceb98a15680911fe1c47ffb57c4b840?fid=3730888783-250528-248677775457729&time=1555401600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-5p5VfQnq5iPOkUOqx1tl%2FNL6Ch8%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2450712839096777272&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

1.10 Sizes
---

Using plt.scatter(x,y,s=?) to define the size of your scatter plot.

Example 

*Python script*

```
# Import numpy as np
import numpy as np

# Store pop as a numpy array: np_pop
np_pop = np.array(pop)

# Double np_pop
np_pop = np_pop * 2

# Update: set s argument to np_pop
plt.scatter(gdp_cap, life_exp, s = np_pop)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000, 10000, 100000],['1k', '10k', '100k'])

# Display the plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/cd5be1be8330e9b71ff71fb20f2007db?fid=3730888783-250528-568015039259451&time=1555401600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-Xr5tUqKQ4bVmENv6m4efW%2B62o%2Bg%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2450795121811247622&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)



1.11 Colors
---

Change the colors of your scatter plot. plt.scatter(x,y,s=10,c = col)
Change the opacity of your scatter plot. plt.scatter(x,y,s=10,c=col,alpha = 0.8)

Example 

Firts to build a dict for your colors.
```
dict = {
    'Asia':'red',
    'Europe':'green',
    'Africa':'blue',
    'Americas':'yellow',
    'Oceania':'black'
}
```

Then
```
# Specify c and alpha inside plt.scatter()
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Show the plot
plt.show()
```

*Ipythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/481d1ccafb403640ad7e719a42472d4b?fid=3730888783-250528-218009850456971&time=1555401600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-2i1ajBk%2BPWxj%2BeVvEF%2Bnnjd7w%2BM%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2450923778292283026&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)


1.12 Additional Customizations
---

Use plt.text() to add words.
Use plt.grid(True) to calls the gridlines.

Example

*Python script*

```
# Scatter plot
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Additional customizations
plt.text(1550, 71, 'India')
plt.text(5700, 80, 'China')

# Add grid() call
plt.grid(True)

# Show the plot
plt.show()
```

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/0ff050d6d8bc8b21329c7711049909ee?fid=3730888783-250528-534066679406179&time=1555401600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-DaDaLB7eOfrwKT4yO7c0RNao%2F0Y%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2451140943484299420&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)




