# pandas.DataFrame

`class pandas.DataFrame(data = None, index = None, columns = None, dtype = None, copy = None)`.

# Parameters(in Simple Terms)

1. `data` : The actual data to use. Can be dictionary, list, array or another DataFrame.

2. `Index` : Row Labels. If not given, pandas will use default numbers like 0, 1, 2..

3. `Columns` : Columns labels. If not given, pandas tries to figure them out or uses default numbers.

4. `dtype` : We can set the data type(like `int, float, str`). If not set, pandas will guess.

5. `Copy` : Whether to copy the data or not. Usually, you don't need to worry about this.


# pandas.DataFrame.from_records

```
classmethod DataFrame.from_records(data, index = None, exclude=None, columns=None, coerce_float=False, nrows=None)
```
- Convert structured or record ndarray to DataFrame.
- Creates a DataFrame object from a structured ndarray, sequecnce or tuples or dict, or DataFrame.

# Parameters

1. `data` : Structured ndarray, sequence of tuples or dicts, or DataFrame Structured input data.

2. `index` : str, list of fields, array-like. Field of array to use as the index, alternately a specific set of input labels to use.

3. `exclude` : sequence, default None. Columns or fields to exclude.

4. `coerce_float` : bool, default False. Attem to convert values of non-string, non-numeric objects(like decimal.Decimal) to floating point, useful for SQL result sets.

5. `nrows` : int, default None. Number of rows to read if data
is an iterator.

**Example** : Data can be provided as a structured ndarray.

```
import numpy as np
import pandas as pd
data = np.array([(3, 'a'), (2, 'b'), (1, 'c'), (0, 'd')], dtype = [('col_1', 'i4'), ('col_2', 'U1')])
pd.DataFrame.from_records(data)
```

**Output** : 
|       | col_1 | col_2 |
|-------|-------|-------|
|   0   |   3   |   a   |
|   1   |   2   |   b   |
|   2   |   1   |   c   |
|   3   |   0   |   d   |


**Daata can be provided as a list of dicts**
```
import pandas as pd
data = [{'col_1':3, 'col_2':'a'},
         {'col_1':2, 'col_2':'b'},
         {'col_1':1, 'col_2':'c'},
         {'col_1':0, 'col_2':'d'}]
pd.DataFrame.from_records(data)
```

**Output**
|       | col_1 | col_2 |
|-------|-------|-------|
|   0   |   3   |   a   |
|   1   |   2   |   b   |
|   2   |   1   |   c   |
|   3   |   0   |   d   |


**Data can be provided as a list of tuples with corresponding columns**.
```
import pandas as pd
import numpy as np
data = [(3, 'a'), (2, 'b'), (1, 'c'), (0, 'd')]
pd.DataFrame.from_records(data, columns=['col_1','col_2'])
```
**Output**
|       | col_1 | col_2 |
|-------|-------|-------|
|   0   |   3   |   a   |
|   1   |   2   |   b   |
|   2   |   1   |   c   |
|   3   |   0   |   d   |
