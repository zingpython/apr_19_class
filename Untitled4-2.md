

```python
import pandas as pd
```


```python
cities = ["Bangor", "Boston","Baltimore", "Boca Raton"]
```


```python
states = ["MA", "MS","MD", "FL"]
```


```python
population = [1.0,1.5,0.75,0.35]
```


```python
visitors = [139,237,362,456]
```


```python
list_labels = ["City","State", "Population","Visitors"]
```


```python
list_cols = [cities,states,population,visitors]
```


```python
zipped = list(zip(list_labels, list_cols))
```


```python
zipped
```




    [('City', ['Bangor', 'Boston', 'Baltimore', 'Boca Raton']),
     ('State', ['MA', 'MS', 'MD', 'FL']),
     ('Population', [1.0, 1.5, 0.75, 0.35]),
     ('Visitors', [139, 237, 362, 456])]




```python
data = dict(zipped)
data
```




    {'City': ['Bangor', 'Boston', 'Baltimore', 'Boca Raton'],
     'Population': [1.0, 1.5, 0.75, 0.35],
     'State': ['MA', 'MS', 'MD', 'FL'],
     'Visitors': [139, 237, 362, 456]}




```python
df = pd.DataFrame(data)
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Population</th>
      <th>State</th>
      <th>Visitors</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Bangor</td>
      <td>1.00</td>
      <td>MA</td>
      <td>139</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Boston</td>
      <td>1.50</td>
      <td>MS</td>
      <td>237</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Baltimore</td>
      <td>0.75</td>
      <td>MD</td>
      <td>362</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Boca Raton</td>
      <td>0.35</td>
      <td>FL</td>
      <td>456</td>
    </tr>
  </tbody>
</table>
</div>




```python
# broadcasting, broadcasts to entire column
df["Attractions"] = ""
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Population</th>
      <th>State</th>
      <th>Visitors</th>
      <th>Attractions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Bangor</td>
      <td>1.00</td>
      <td>MA</td>
      <td>139</td>
      <td></td>
    </tr>
    <tr>
      <th>1</th>
      <td>Boston</td>
      <td>1.50</td>
      <td>MS</td>
      <td>237</td>
      <td></td>
    </tr>
    <tr>
      <th>2</th>
      <td>Baltimore</td>
      <td>0.75</td>
      <td>MD</td>
      <td>362</td>
      <td></td>
    </tr>
    <tr>
      <th>3</th>
      <td>Boca Raton</td>
      <td>0.35</td>
      <td>FL</td>
      <td>456</td>
      <td></td>
    </tr>
  </tbody>
</table>
</div>




```python
# we can change index
df.index = ["a","b","c","d"]
df
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>City</th>
      <th>Population</th>
      <th>State</th>
      <th>Visitors</th>
      <th>Attractions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>Bangor</td>
      <td>1.00</td>
      <td>MA</td>
      <td>139</td>
      <td></td>
    </tr>
    <tr>
      <th>b</th>
      <td>Boston</td>
      <td>1.50</td>
      <td>MS</td>
      <td>237</td>
      <td></td>
    </tr>
    <tr>
      <th>c</th>
      <td>Baltimore</td>
      <td>0.75</td>
      <td>MD</td>
      <td>362</td>
      <td></td>
    </tr>
    <tr>
      <th>d</th>
      <td>Boca Raton</td>
      <td>0.35</td>
      <td>FL</td>
      <td>456</td>
      <td></td>
    </tr>
  </tbody>
</table>
</div>




```python

```
