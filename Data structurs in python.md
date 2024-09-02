### Series
One dimensional data structure with labelled enteries. Capable of holding any kind of data type. Needs to be imported

```
import pandas as pd
pd.series(Data, index=<labels>)
```


The data can be of the form or a scalar value such as int char string, etc or values such as arrays, dictionary, lists

When defining a series with a dictionary, the index is the name of the dictionary definition and the data for that index is the dictionary value 

### Dataframe
Two dimentional data structure
A dataframe can have
- A dictionary of 1d arrays, lists, dictionaries or series
- 2dn array
- a series
- a dataframe


```
import pandas as pd
pd.DataFrame(Data, index=<labels>)
```

Lists and so on take the columns, indices are the name of the rows. a dictionary of lists is used to name the columns
