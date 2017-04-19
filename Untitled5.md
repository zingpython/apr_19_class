

```python
#import pandas
import pandas as pd 
```


```python
# create Data Frame object
stocks = ["IBM", "APPLE", "TWTTR", "GE", "MSFT"]
prices = [115.00, 119.14, 19.77, 25.99, 26]
```


```python
portfolio = list(zip(stocks,prices))
print(portfolio)
```

    [('IBM', 115.0), ('APPLE', 119.14), ('TWTTR', 19.77), ('GE', 25.99), ('MSFT', 26)]



```python
df = pd.DataFrame(data=portfolio, columns=['stocks', 'prices'])
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stocks</th>
      <th>prices</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>IBM</td>
      <td>115.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>APPLE</td>
      <td>119.14</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWTTR</td>
      <td>19.77</td>
    </tr>
    <tr>
      <th>3</th>
      <td>GE</td>
      <td>25.99</td>
    </tr>
    <tr>
      <th>4</th>
      <td>MSFT</td>
      <td>26.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
type(df)
```




    pandas.core.frame.DataFrame




```python
# returns number of rows and columns
df.shape
```




    (5, 2)




```python
# returns name of columns
df.columns
```




    Index(['stocks', 'prices'], dtype='object')




```python
#lets add another col
df['new_col'] = " "
df['new_col'] = 5

print(df)
```

      stocks  prices  new_col
    0    IBM  115.00        5
    1  APPLE  119.14        5
    2  TWTTR   19.77        5
    3     GE   25.99        5
    4   MSFT   26.00        5



```python
# access the item by loc
df.loc[2]
```




    stocks     TWTTR
    prices     19.77
    new_col        5
    Name: 2, dtype: object




```python
# slicing df
# loc works on abels in the index.
df.loc[:3]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stocks</th>
      <th>prices</th>
      <th>new_col</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>IBM</td>
      <td>115.00</td>
      <td>5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>APPLE</td>
      <td>119.14</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWTTR</td>
      <td>19.77</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>GE</td>
      <td>25.99</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.iloc[-1:,:]
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stocks</th>
      <th>prices</th>
      <th>new_col</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>MSFT</td>
      <td>26.0</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# lets write this to csv file
df.to_csv("classfile.csv", index=True)
```


```python

```
