# pandas.DataFrame.from_dict

```
classmethod DataFrame.from_dict(data, orient='columns', dtype=None, columns=None)
```
- Construct DataFrame from dict of array-like or dicts.
- Creates DataFrame objects from dictionary by columns or by index allowing dtype specification.

# Parameters

1. `data : dict` = Of the form {field: array-like} or {field:dict}.

2. `orient : {'columns', 'index', 'tight'}, default 'columns' ` : The "orientation" of the data. If the keys of the passed dict should be columns of the resulting DataFrame, pass 'columns'(default). Otherwisw if the keys should be rows, pass 'index'.If 'tight' assume a dict with keys['index','columns','data','index_names','columns_names'].

3. `dtype : dtype, default None` : Data type to force after dataframe construction, otherwise infer.

4. `Columns : list, default None` : Columns labels to use when `orient = 'index'`. Raise a ValueError if used with `orient = 'columns` or `orient = 'tight'`.

**By default the keys of the dict become the DataFrame columns.**
```
import pandas as pd
data = {'col_1': [3, 2, 1, 0], 'col_2' : ['a', 'b', 'c' , 'd']}
pd.DataFrame.from_dict(data)
```

**Output**
```
   col_1 col_2
0      3     a
1      2     b
2      1     c
3      0     d
```

**By default the keys of the dict become the DataFrame Columns**.
```
import pandas as pd
data = {'row_1': [3, 2, 1, 0], 'row_2': ['a', 'b', 'c', 'd']}
pd.DataFrame.from_dict(data, orient = 'index')
```

**Output** :

```
       0  1  2  3
row1  3  2  1  0
row_2  a  b  c  d
```

**When using the 'index' orientation, the columns names can be specified manually.**

```
import pandas as pd
data = {'row_1': [3, 2, 1, 0], 'row_2': ['a', 'b', 'c', 'd']}
pd.DataFrame.from_dict(data, orient = 'index', columns = ['A', 'B', 'C', 'D'])
```

**Output** : 
```
       A  B  C  D
row_1  3  2  1  0
row_2  a  b  c  d
```
