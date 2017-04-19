

```python
dividends = [1, 1.5, 1.75, 0.75, 1.25]
stock_prices = [50, 55, 62, 47, 84]
```


```python
# Dividend Yield = Annual Dividend / Current Stock Price
# can not do dividends/stock_prices
import numpy as np
```


```python
# lets convert lists into numpy arrays
# If you use different types NumPy converts everything to string
np_dividends = np.array(dividends)
np_stock_prices = np.array(stock_prices)
np_stock_prices
```




    array([50, 55, 62, 47, 84])




```python
np_div = np_dividends/np_stock_prices*100
np_div
```




    array([ 2.        ,  2.72727273,  2.82258065,  1.59574468,  1.48809524])




```python
# NumPy behaves differently than Python

a = [1,2,3]
b = [4,5,6]
c = a + b
c
```




    [1, 2, 3, 4, 5, 6]




```python
# NumPy adds items
b = np.array(b)
c = a + b
print(c)
c
```

    [5 7 9]





    array([5, 7, 9])




```python
np_div[1]
```




    2.7272727272727271




```python
np_div > 2.72
```




    array([False,  True,  True, False, False], dtype=bool)




```python
np_div[np_div > 2.72]
```




    array([ 2.72727273,  2.82258065])




```python
# 2D NumPy Arrays
# ndarray stands for N-dimensional array
type(np_div)
```




    numpy.ndarray




```python
# we can create 2d array from a regular python list of lists
np_2d = np.array([[1, 1.5, 1.75, 0.75, 1.25],[50, 55, 62, 47, 84]])
np_2d
```




    array([[  1.  ,   1.5 ,   1.75,   0.75,   1.25],
           [ 50.  ,  55.  ,  62.  ,  47.  ,  84.  ]])




```python
# we got rectangular data structure
# lets see how many rows and colums using shape
np_2d.shape
```




    (2, 5)




```python
# with a 2d array we can do indexing 
np_2d[0]
```




    array([ 1.  ,  1.5 ,  1.75,  0.75,  1.25])




```python
np_2d[1][1]
```




    55.0




```python
# or you could subsetting
# [row,column]
np_2d[1,1]
```




    55.0




```python
# or we could get entire second row
np_2d[1,:]
```




    array([ 50.,  55.,  62.,  47.,  84.])




```python
# Similarly we can use mean and median functions for the whole row 
avarage_stock_price = np.mean(np_2d[1,:])
avarage_stock_price
```




    59.600000000000001




```python
# generate data
# (distribution mean, standard dev., number of samples)

prices = np.round(np.random.normal(50, 0.20, 10), 2)
prices
```




    array([ 49.68,  50.24,  49.92,  50.1 ,  49.69,  50.11,  49.79,  49.87,
            50.  ,  49.54])




```python
dividends = np.round(np.random.normal(1.25, 0.20, 10), 2)
dividends
```




    array([ 1.26,  1.25,  1.39,  1.35,  1.16,  1.05,  1.56,  1.25,  1.54,  1.19])




```python
# create two columns
portfolio = np.column_stack((prices, dividends))
portfolio
```




    array([[ 49.68,   1.26],
           [ 50.24,   1.25],
           [ 49.92,   1.39],
           [ 50.1 ,   1.35],
           [ 49.69,   1.16],
           [ 50.11,   1.05],
           [ 49.79,   1.56],
           [ 49.87,   1.25],
           [ 50.  ,   1.54],
           [ 49.54,   1.19]])




```python

```
