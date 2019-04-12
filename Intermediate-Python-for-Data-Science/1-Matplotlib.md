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
`
# Print the last item of gdp_cap and life_exp
print(gdp_cap[-1])
print(life_exp[-1])

# Make a line plot, gdp_cap on the x-axis, life_exp on the y-axis
plt.plot(gdp_cap,life_exp)

# Display the plot
plt.show()
`

*IPythonshell*
`
<script.py> output:
    469.70929810000007
    43.487
`
![avatar](https://thumbnail0.baidupcs.com/thumbnail/f286a2ee8abbf3fded76937cc3a40b2e?fid=3730888783-250528-929140149197988&time=1555056000&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-zeGhiB0g5xPdpZlF9blTCOSKPrQ%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2358847365947123499&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

1.3 Scatter Plot
---

Use plt.scatter() tu build a scatterplot.
For a better view, use plt.xscale() to give the better scale for a better view.

Example

a.If you do not change the xscale

*Python script*
`
# Change the line plot below to a scatter plot
plt.scatter(gdp_cap, life_exp)

# Put the x-axis on a logarithmic scale

# Show plot
plt.show()
`

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/f41f0439c3f0378d8f4310b3dc16ab2c?fid=3730888783-250528-312668319005379&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-seVZeQMWJeAyaafSj06az36VxH0%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2358965791052885975&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

b.If you change the x-scale

*Python script*
`
# Change the line plot below to a scatter plot
plt.scatter(gdp_cap, life_exp)

# Put the x-axis on a logarithmic scale
plt.xscale('log')

# Show plot
plt.show()
`

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
`
# Import package
import matplotlib.pyplot as plt

# Build Scatter plot
plt.scatter(pop,life_exp)

# Show plot
plt.show()
`

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4cfdc5ec2a29b9d666d3b42a8b30f055?fid=3730888783-250528-1013308925970959&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-3WI6kkbbD73vw9i2QRD7vMQQmTQ%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359057980934801264&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)


1.5 Build a Histogram
---

Use plt.hist() to build the histogram.
Use plt.show() to show the graphy.

*Python script*
`
# Create histogram of life_exp data
plt.hist(life_exp)

# Display histogram
plt.show()
`

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
`
# Build histogram with 5 bins
plt.hist(life_exp, bins = 5)

# Show and clean up plot
plt.show()


# Build histogram with 20 bins
plt.hist(life_exp, bins = 20)

# Show and clean up again
plt.show()
`

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4d07dd2414ebe6b8cd07c78836c1c6d2?fid=3730888783-250528-275116827184735&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-PmA7z5FwdRY1JTMAX5Nj%2BqtlHqo%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359287451383994724&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

![avatar](https://thumbnail0.baidupcs.com/thumbnail/2a20e92ad2c29815ea51a171452028cb?fid=3730888783-250528-222187959145345&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-SY1laNpUJlT0n1YcvOrIfWGGO1Q%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359320513403493981&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

b.if you use plt.clf to clean the last picture.

*Python script*
`
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
`

*IPythonshell*

![avatar](https://thumbnail0.baidupcs.com/thumbnail/4d07dd2414ebe6b8cd07c78836c1c6d2?fid=3730888783-250528-275116827184735&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-PmA7z5FwdRY1JTMAX5Nj%2BqtlHqo%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359287451383994724&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)

![avatar](https://thumbnail0.baidupcs.com/thumbnail/d6d867be56df44e89583c18ecaec92a0?fid=3730888783-250528-639985530350509&time=1555059600&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-eIsTGHORsULhdxNOC%2FizkdTFyyw%3D&expires=8h&chkv=0&chkbd=0&chkpc=&dp-logid=2359298981216199442&dp-callid=0&size=c710_u400&quality=100&vuk=-&ft=video)
