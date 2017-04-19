

```python
import numpy as np
import pandas as pd
```


```python
 s = pd.Series(np.random.randn(5), index=['a', 'b', 'c', 'd', 'e'])
```


```python
s
```




    a    0.274828
    b   -0.017681
    c   -0.094049
    d   -0.487026
    e    0.230908
    dtype: float64




```python
s*(-1)
```




    a   -0.274828
    b    0.017681
    c    0.094049
    d    0.487026
    e   -0.230908
    dtype: float64




```python
s[0]
```




    0.27482785102493767




```python
s[2:3]
```




    c   -0.094049
    dtype: float64




```python
s[[4, 3, 1]]
```




    e    0.230908
    d   -0.487026
    b   -0.017681
    dtype: float64




```python

```
