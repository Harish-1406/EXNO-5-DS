# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
## Line Plot
```py
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
```py
# CREATE A LINE GRAPH FOR X AND Y AND LABEL X axis and Y Axis and create a legend
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x,y)
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.show()
```

<img width="554" height="432" alt="image" src="https://github.com/user-attachments/assets/74857722-aac1-4f0a-85d4-39c194baec47" />

```py

# line 1 points
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
# plot line 1 and line 2 points in same graph and include the necessary parameters

plt.plot(x1,y1,color='red',label='line-1')
plt.plot(x2,y2,color='blue',label='line-2')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Two lines on the same graph')
plt.legend()
plt.show()
```

<img width="567" height="453" alt="image" src="https://github.com/user-attachments/assets/fa5f7f61-91ce-4666-b416-b6f881168f0d" />

## Bar Chart
```py
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
c1 =['red', 'green']
c2 =['b', 'g']
plt.bar (names, values, width=0.7, color=c1)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('Bar chart representation')
plt.show()
```

<img width="554" height="453" alt="image" src="https://github.com/user-attachments/assets/b92bb3f3-5542-483c-96e5-ece3fc1955e4" />

## Spline 
```py
import numpy as np
from scipy.interpolate import make_interp_spline
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])
spline=make_interp_spline(x,y)
x_smooth=np.linspace(x.min(),x.max(),100)
y_smooth=spline(x_smooth)
plt.plot(x,y,'o',label='Data values',color='b')
plt.plot(x_smooth,y_smooth,'-',label='spline',color='black')
plt.legend()
plt.show()
```

<img width="543" height="413" alt="image" src="https://github.com/user-attachments/assets/6e592027-730e-4950-a159-08082b01517e" />

```py
# CREATE A SCATTER PLOT FOR X_VALUES AND Y_VALUES
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter(x_values,y_values,label='data',marker='o',color='red')
plt.legend()
plt.show()
```

<img width="543" height="413" alt="image" src="https://github.com/user-attachments/assets/e31f2bd5-954c-48ca-b1f2-0093e5867d34" />

```py
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label='stars',color='green',marker='*',s=30)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.legend()
plt.show()
```

<img width="563" height="432" alt="image" src="https://github.com/user-attachments/assets/77b99805-d412-4e9c-9c37-64d6ba212f7f" />

## Pie Chart
```py
activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']
plt.pie(slices,labels=activities,colors=colors,startangle=90,shadow=True,autopct='%1.1f%%')
plt.legend()
plt.show()
```

<img width="402" height="389" alt="image" src="https://github.com/user-attachments/assets/9a90b82a-d148-443b-a068-e98487701cb3" />

# Result:
From this experiment , I have learnt that how the different plots in data visualization works effectively.Like how Line chart and Spline chart helps to show the trends and relationships between variables. Also these visualization helps to discover trends and patterns that help to analyse the data.
