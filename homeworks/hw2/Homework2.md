```python
import numpy as np
```


```python
values = [23, 19, 34, 50]
```


```python
np_values = np.array(values)
print(np_values)
```

    [23 19 34 50]
    


```python
x = np.arange(12,36)
print(x)
```

    [12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35]
    


```python
x2 = np.arange(10,19,2)
print(x2)
```

    [10 12 14 16 18]
    


```python
x3 = np.arange(8,-4,-1)
print(x3)
```

    [ 8  7  6  5  4  3  2  1  0 -1 -2 -3]
    


```python
mpg = np.array([19, 23, 20, 21, 20, 23, 21, 21, 23, 19, 24, 23, 28, 19, 18, 21, 23, 17, 20, 20, 20, 21, 24, 18, 15])
```


```python
print(mpg[3:10])
```

    [21 20 23 21 21 23 19]
    


```python
print(mpg[15:])
```

    [21 23 17 20 20 20 21 24 18 15]
    


```python
goodMpg = mpg[mpg >= 23]
print(goodMpg)
```

    [23 23 23 24 23 28 23 24]
    


```python

okMpg = mpg[(mpg > 18) & (mpg < 23)]
print(okMpg)
```

    [19 20 21 20 21 21 19 19 21 20 20 20 21]
    [19 20 21 20 21 21 19 19 21 20 20 20 21]
    


```python
kpl = mpg * 0.425
print(kpl)
```

    [ 8.075  9.775  8.5    8.925  8.5    9.775  8.925  8.925  9.775  8.075
     10.2    9.775 11.9    8.075  7.65   8.925  9.775  7.225  8.5    8.5
      8.5    8.925 10.2    7.65   6.375]
    


```python
A = np.arange(2,11).reshape(3,3)
print(A)
```

    [[ 2  3  4]
     [ 5  6  7]
     [ 8  9 10]]
    


```python
A[(A > 3) & (A<7)] = -A[(A > 3) & (A < 7)]
print(A)
```

    [[ 2  3 -4]
     [-5 -6  7]
     [ 8  9 10]]
    


```python
print(A[0])
```

    [ 2  3 -4]
    


```python
print(A[:,2].reshape(3,1))
```

    [[-4]
     [ 7]
     [10]]
    


```python
print(np.sum(A[:,1]))
```

    6
    


```python
print(np.mean(A)) # prints average in mean
```

    2.6666666666666665
    


```python
print(np.median(A[:,1]))
```

    3.0
    


```python
row = np.array([-2,1,2])
result = A + row
print(result)
```

    [[ 0  4 -2]
     [-7 -5  9]
     [ 6 10 12]]
    


```python
B = np.arange(24).reshape(4,3,2)
print(B)
```

    [[[ 0  1]
      [ 2  3]
      [ 4  5]]
    
     [[ 6  7]
      [ 8  9]
      [10 11]]
    
     [[12 13]
      [14 15]
      [16 17]]
    
     [[18 19]
      [20 21]
      [22 23]]]
    


```python

```
