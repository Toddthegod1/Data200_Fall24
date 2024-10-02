```python
import numpy as pd
import pandas as pd
```


```python
data = {
  'animal': ['cat','cat','snake','dog', 'dog','cat','snake','cat','dog','dog'],
  'age': [2.5, 3, 0.5, 7, 5, 2, 4.5, 4, 7, 3],
  'visits': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
  'priority': ['yes','yes','no','yes','no',
  'no','no','yes','no', 'no']}
```


```python
row_names = pd.Index(pet_names)
pet_names = ['Maisey', 'Finny', 'Slithery', 'Fluffy', 'Rex', 'Tucker', 'Snakey', 
             'Mason', 'Lou Lou', 'Snoopy']
name = pet_names
vetInfo = pd.DataFrame(data, index = row_names)
print(vetInfo)
```

             animal  age  visits priority
    Maisey      cat  2.5       1      yes
    Finny       cat  3.0       3      yes
    Slithery  snake  0.5       2       no
    Fluffy      dog  7.0       3      yes
    Rex         dog  5.0       2       no
    Tucker      cat  2.0       3       no
    Snakey    snake  4.5       1       no
    Mason       cat  4.0       1      yes
    Lou Lou     dog  7.0       2       no
    Snoopy      dog  3.0       1       no
    


```python
vetInfo[2:5]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Slithery</th>
      <td>snake</td>
      <td>0.5</td>
      <td>2</td>
      <td>no</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Rex</th>
      <td>dog</td>
      <td>5.0</td>
      <td>2</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo[['animal','age']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>2.5</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>Slithery</th>
      <td>snake</td>
      <td>0.5</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>Rex</th>
      <td>dog</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>Tucker</th>
      <td>cat</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>Snakey</th>
      <td>snake</td>
      <td>4.5</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>Lou Lou</th>
      <td>dog</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>Snoopy</th>
      <td>dog</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo.iloc[2:5]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Slithery</th>
      <td>snake</td>
      <td>0.5</td>
      <td>2</td>
      <td>no</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Rex</th>
      <td>dog</td>
      <td>5.0</td>
      <td>2</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo.iloc[:2]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>2.5</td>
      <td>1</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo.loc[['Maisey', 'Finny', 'Snoopy']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>2.5</td>
      <td>1</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Snoopy</th>
      <td>dog</td>
      <td>3.0</td>
      <td>1</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo.loc[['Slithery','Snakey'], ['age', 'visits']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>visits</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Slithery</th>
      <td>0.5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>Snakey</th>
      <td>4.5</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo[vetInfo['age'] > 3]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Rex</th>
      <td>dog</td>
      <td>5.0</td>
      <td>2</td>
      <td>no</td>
    </tr>
    <tr>
      <th>Snakey</th>
      <td>snake</td>
      <td>4.5</td>
      <td>1</td>
      <td>no</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>4.0</td>
      <td>1</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Lou Lou</th>
      <td>dog</td>
      <td>7.0</td>
      <td>2</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo[vetInfo['priority'] == 'yes']
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>2.5</td>
      <td>1</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>4.0</td>
      <td>1</td>
      <td>yes</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo[(vetInfo['priority'] == 'yes') & (vetInfo['age'] > 3)]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>4.0</td>
      <td>1</td>
      <td>yes</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo.loc[vetInfo['priority'] == 'yes', ['animal', 'visits']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>visits</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>1</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>3</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python
vetInfo['age_visit'] = vetInfo['age'] / vetInfo['visits']
vetInfo
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
      <th>age_visit</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>2.5</td>
      <td>1</td>
      <td>yes</td>
      <td>2.500000</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3.0</td>
      <td>3</td>
      <td>yes</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>Slithery</th>
      <td>snake</td>
      <td>0.5</td>
      <td>2</td>
      <td>no</td>
      <td>0.250000</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
      <td>2.333333</td>
    </tr>
    <tr>
      <th>Rex</th>
      <td>dog</td>
      <td>5.0</td>
      <td>2</td>
      <td>no</td>
      <td>2.500000</td>
    </tr>
    <tr>
      <th>Tucker</th>
      <td>cat</td>
      <td>2.0</td>
      <td>3</td>
      <td>no</td>
      <td>0.666667</td>
    </tr>
    <tr>
      <th>Snakey</th>
      <td>snake</td>
      <td>4.5</td>
      <td>1</td>
      <td>no</td>
      <td>4.500000</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>4.0</td>
      <td>1</td>
      <td>yes</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>Lou Lou</th>
      <td>dog</td>
      <td>7.0</td>
      <td>2</td>
      <td>no</td>
      <td>3.500000</td>
    </tr>
    <tr>
      <th>Snoopy</th>
      <td>dog</td>
      <td>3.0</td>
      <td>1</td>
      <td>no</td>
      <td>3.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
mean = vetInfo['age'].mean()
print('The average age of the animals is', mean)
```

    The average age of the animals is 3.85
    


```python
dogsCats = vetInfo[vetInfo["animal"].isin(['cat', 'dog'])]
dogsCats
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>animal</th>
      <th>age</th>
      <th>visits</th>
      <th>priority</th>
      <th>age_visit</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Maisey</th>
      <td>cat</td>
      <td>2.5</td>
      <td>1</td>
      <td>yes</td>
      <td>2.500000</td>
    </tr>
    <tr>
      <th>Finny</th>
      <td>cat</td>
      <td>3.0</td>
      <td>3</td>
      <td>yes</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>Fluffy</th>
      <td>dog</td>
      <td>7.0</td>
      <td>3</td>
      <td>yes</td>
      <td>2.333333</td>
    </tr>
    <tr>
      <th>Rex</th>
      <td>dog</td>
      <td>5.0</td>
      <td>2</td>
      <td>no</td>
      <td>2.500000</td>
    </tr>
    <tr>
      <th>Tucker</th>
      <td>cat</td>
      <td>2.0</td>
      <td>3</td>
      <td>no</td>
      <td>0.666667</td>
    </tr>
    <tr>
      <th>Mason</th>
      <td>cat</td>
      <td>4.0</td>
      <td>1</td>
      <td>yes</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>Lou Lou</th>
      <td>dog</td>
      <td>7.0</td>
      <td>2</td>
      <td>no</td>
      <td>3.500000</td>
    </tr>
    <tr>
      <th>Snoopy</th>
      <td>dog</td>
      <td>3.0</td>
      <td>1</td>
      <td>no</td>
      <td>3.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
cd "C:\Users\toddj\Downloads\Data200_Fall24-main\Data200_Fall24-main\data"
```

    C:\Users\toddj\Downloads\Data200_Fall24-main\Data200_Fall24-main\data
    


```python
motorTrend = pd.read_csv('MotorTrend.csv')
```


```python
motorTrend = df.motorTrend
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[189], line 1
    ----> 1 motorTrend = df.motorTrend
    

    NameError: name 'df' is not defined



```python
print(motorTrend.shape)
```

    (32, 12)
    


```python
motorTrend.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>mpg</th>
      <th>cyl</th>
      <th>disp</th>
      <th>hp</th>
      <th>drat</th>
      <th>wt</th>
      <th>qsec</th>
      <th>vs</th>
      <th>am</th>
      <th>gear</th>
      <th>carb</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Mazda RX4</td>
      <td>21.0</td>
      <td>6</td>
      <td>160.0</td>
      <td>110</td>
      <td>3.90</td>
      <td>2.620</td>
      <td>16.46</td>
      <td>0</td>
      <td>manual</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Mazda RX4 Wag</td>
      <td>21.0</td>
      <td>6</td>
      <td>160.0</td>
      <td>110</td>
      <td>3.90</td>
      <td>2.875</td>
      <td>17.02</td>
      <td>0</td>
      <td>manual</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Datsun 710</td>
      <td>22.8</td>
      <td>4</td>
      <td>108.0</td>
      <td>93</td>
      <td>3.85</td>
      <td>2.320</td>
      <td>18.61</td>
      <td>1</td>
      <td>manual</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Hornet 4 Drive</td>
      <td>21.4</td>
      <td>6</td>
      <td>258.0</td>
      <td>110</td>
      <td>3.08</td>
      <td>3.215</td>
      <td>19.44</td>
      <td>1</td>
      <td>auto</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Hornet Sportabout</td>
      <td>18.7</td>
      <td>8</td>
      <td>360.0</td>
      <td>175</td>
      <td>3.15</td>
      <td>3.440</td>
      <td>17.02</td>
      <td>0</td>
      <td>auto</td>
      <td>3</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>




```python
motorTrend[['mpg', 'hp']].describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>mpg</th>
      <th>hp</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>32.000000</td>
      <td>32.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>20.090625</td>
      <td>146.687500</td>
    </tr>
    <tr>
      <th>std</th>
      <td>6.026948</td>
      <td>68.562868</td>
    </tr>
    <tr>
      <th>min</th>
      <td>10.400000</td>
      <td>52.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>15.425000</td>
      <td>96.500000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>19.200000</td>
      <td>123.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>22.800000</td>
      <td>180.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>33.900000</td>
      <td>335.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
