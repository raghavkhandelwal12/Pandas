# DataFrame

- A `DataFrame` is a 2-dimensional `labeled data structure` in pandas that looks like a table(rows and columns), similar to an excel spreadsheet or sql table.

# Create a DataFrame using the list

- A list of lists or a list of values can be used.
- When using a `list of lists`,each inner list becomes a row.

```
#list of lists(rows)
import pandas as pd
data = [["Alice", 24], ["Bob", 27], ["Charlie", 22]]
df = pd.DataFrame(data, columns = ["Name", "Age"])
print(df)
```
**Output**
```
Name  Age
0    Alice   24
1      Bob   27
2  Charlie   22
```

**List of Values(1D)**
```
import pandas as pd
data = [10, 20, 30, 40, 50]
df = pd.DataFrame(data, columns = ["Score"])
print(df)
```

**Output**
```
Score
0     10
1     20
2     30
3     40
4     50
```

# Using a Tuple

- Similar to lists, tuples can be used inside lists or dictionaries.
- A list of tuples works the same as list of lists.

**List of tuples**

```
import pandas as pd
data = [('Alice', 24), ('Bob', 27), ('Charlie', 22)]
df = pd.DataFrame(data, columns = ['Name', 'Age'])
print(df)
```

**Output**
```
Name  Age
0    Alice   24
1      Bob   27
2  Charlie   22
```

**Tuples of Tuples**
```
import pandas as pd
data = (('Math', 85), ('Science', 90), ('Physics', 78))
df = pd.DataFrame(data, columns = ['Subject', 'Marks'])
print(df)
```

**Output**
```
Subject  Marks
0     Math     85
1  Science     90
2  Physics     78
```

# Using a Dictionary

- Most commonly used method.
- Key become columns name; values become data.
- Each key map to a list(or another structure) of column values.

**Dictionary of lists(columns)**
```
import pandas as pd
data = {
    'Name' : ['Alice', 'Bob', 'Charlie'],
    'Age'  : [24, 27, 22],
    'City' : ['NYC', 'LA', 'Chicago']
}
df = pd.DataFrame(data)
print(df)
```

**Output**
```
Name  Age     City
0    Alice   24      NYC
1      Bob   27       LA
2  Charlie   22  Chicago
```

**Dictionary of Tuples**

```
import pandas as pd
data = {
    'Product' : ('Laptop', ' Phone', 'Tablet'),
    'Price' : (1000, 700, 300)
}
df = pd.DataFrame(data)
print(df)
```

**Output**
```
Product  Price
0  Laptop   1000
1   Phone    700
2  Tablet    300
```

**Construction DataFrame from a dictionary**

```
import pandas as pd
d = {'col1':[1,2], 'col2':[3,4]}
df = pd.DataFrame(data = d)
print(df)
```

**Output** : 
```
   col1  col2
0     1     3
1     2     4
```

**Notice that infer dtype is int64**

```
import pandas as pd
d = {'col1':[1,2], 'col2':[3,4]}
df = pd.DataFrame(data = d)
print(df)
print(df.dtypes)
```

**Output** : 
```
   col1  col2
0     1     3
1     2     4
col1    int64
col2    int64
dtype: object
```

**Construction DataFrame from a dictionary including series**
```
import pandas as pd
d = {'col1' : [0,1,2,3], 'col2' : pd.Series([2,3], index = [2,3])}
pd.DataFrame(data = d, index = [0, 1, 2, 3])
```
**Output**
```
   col1  col2
0     0   NaN
1     1   NaN
2     2   2.0
3     3   3.0
```

**Construction DataFrame from numpy ndarray**

```
import pandas as pd
df2 = pd.DataFrame(np.array([[1,2,3],[4,5,6],[7,8,9]]), columns=['a','b','c'])
print(df2)
```

**Output**

```
   a  b  c
0  1  2  3
1  4  5  6
2  7  8  9
```
