# Python Basics


## Snipets

### GetCurrentWeek

    
```python
import datetime
cd =datetime.datetime.now()
cw = cd.isocalendar()[1]
print(cw) 
```


## Strings

`words = s.split(' ')` - split words by space.


## List

```python
arr = [0]*2 #Init 1D arr
arr = [0]*2 #Init 1D arr
arr.append([-1]) # Add append to array
```


## 2D Array

```python
# Python 3 program to demonstrate working
# of method 1 and method 2.
rows, cols = (5, 5)
# method 2 1st approach
arr = [[0]*cols]*rows
# lets change the first element of the
# first row to 1 and print the array
arr[0][0] = 1

for row in arr:
	print(row)
# outputs the following
#[1, 0, 0, 0, 0]
#[1, 0, 0, 0, 0]
#[1, 0, 0, 0, 0]
#[1, 0, 0, 0, 0]
#[1, 0, 0, 0, 0]

# method 2 2nd approach
arr = [[0 for i in range(cols)] for j in range(rows)]

# again in this new array lets change
# the first element of the first row
# to 1 and print the array
arr[0][0] = 1
for row in arr:
	print(row)

# outputs the following as expected
#[1, 0, 0, 0, 0]
#[0, 0, 0, 0, 0]
#[0, 0, 0, 0, 0]
#[0, 0, 0, 0, 0]
#[0, 0, 0, 0, 0]
```
