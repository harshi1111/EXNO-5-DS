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

```
from google.colab import drive
drive.mount('/content/drive')
```

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```
```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
```

```
# CREATE A LINE GRAPH FOR X AND Y AND LABEL X axis and Y Axis and create a legend
plt.plot(x, y, label='Line 1')  # Plotting the line
plt.xlabel('X Axis')  # Labeling the X axis
plt.ylabel('Y Axis')  # Labeling the Y axis
plt.legend()  # Displaying the legend
plt.show()
```

![image](https://github.com/user-attachments/assets/703e53ce-37cc-4b8b-b622-082b9b0f4237)

```
# line 1 points
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
```
```
# plot line 1 and line 2 points in same graph and include the necessary parameters
plt.plot(x1, y1, label='Line 1')  # Plotting Line 1
plt.plot(x2, y2, label='Line 2')  # Plotting Line 2
plt.xlabel('X Axis')  # Labeling the X axis
plt.ylabel('Y Axis')  # Labeling the Y axis
plt.legend()  # Displaying the legend
plt.show()
```

![image](https://github.com/user-attachments/assets/9ca9bc9d-9c47-42ca-900e-11baa2581e11)

```
# plot the points in the above graph
plt.scatter(x1, y1, color='blue', label='Points Line 1')  # Plotting points for Line 1
plt.scatter(x2, y2, color='red', label='Points Line 2')  # Plotting points for Line 2
plt.xlabel('X Axis')  # Labeling the X axis
plt.ylabel('Y Axis')  # Labeling the Y axis
plt.legend()  # Displaying the legend
plt.show()
```

![image](https://github.com/user-attachments/assets/b90b4cb1-d0d2-43f7-9015-6ca7d51cb91f)


```
# Creating some random data
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]


x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
```

```
# implement line graph using fill between option
plt.plot(x_values, y_values, label='Line with Fill')
plt.fill_between(x_values, y_values, color='lightblue', alpha=0.5)  # Filling the area under the curve
plt.xlabel('X Axis')  # Labeling the X axis
plt.ylabel('Y Axis')  # Labeling the Y axis
plt.legend()  # Displaying the legend
plt.show()

from scipy.interpolate import make_interp_spline
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])
```

![image](https://github.com/user-attachments/assets/9fda629c-aa5f-4512-8805-676a8b723d79)


```
# interpolate data using cubic spline
spl = make_interp_spline(x, y, k=3)  # Cubic spline interpolation
x_new = np.linspace(x.min(), x.max(), 500)  # Create new x values for smooth curve
y_new = spl(x_new)  # Get interpolated y values
```

```
# Plotting the original and interpolated curve
plt.plot(x, y, 'o', label='Original Data')  # Plotting original data points
plt.plot(x_new, y_new, label='Cubic Spline Interpolation')  # Plotting the smoothed curve
plt.xlabel('X Axis')  # Labeling the X axis
plt.ylabel('Y Axis')  # Labeling the Y axis
plt.legend()  # Displaying the legend
plt.show()
```
![image](https://github.com/user-attachments/assets/280de9fa-92c9-4875-9930-0279173230fe)


# Result:
 Include your result here
