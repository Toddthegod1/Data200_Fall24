Todd Klinger:


```python
import numpy as np
import os
```


```python
ls
```

     Volume in drive C is OS
     Volume Serial Number is F802-CD04
    
     Directory of C:\Users\toddj\OneDrive - Dickinson College\Documents\GitHub\hw1-Toddthegod1\homeworks\hw1\data
    
    09/16/2024  09:09 PM    <DIR>          .
    09/16/2024  09:09 PM    <DIR>          ..
    09/16/2024  09:09 PM               112 babyNames.txt
    09/16/2024  10:53 PM               488 quotes.txt
    09/16/2024  09:09 PM               648 summerDay.txt
                   3 File(s)          1,248 bytes
                   2 Dir(s)  58,184,077,312 bytes free
    


```python
cd "C:\Users\toddj\OneDrive - Dickinson College\Documents\GitHub\hw1-Toddthegod1\homeworks\hw1\data"
```

    C:\Users\toddj\OneDrive - Dickinson College\Documents\GitHub\hw1-Toddthegod1\homeworks\hw1\data
    


```python
ls
```

     Volume in drive C is OS
     Volume Serial Number is F802-CD04
    
     Directory of C:\Users\toddj\OneDrive - Dickinson College\Documents\GitHub\hw1-Toddthegod1\homeworks\hw1\data
    
    09/16/2024  09:09 PM    <DIR>          .
    09/16/2024  09:09 PM    <DIR>          ..
    09/16/2024  09:09 PM               112 babyNames.txt
    09/16/2024  10:53 PM               488 quotes.txt
    09/16/2024  09:09 PM               648 summerDay.txt
                   3 File(s)          1,248 bytes
                   2 Dir(s)  58,184,044,544 bytes free
    


```python
file = open("quotes.txt", "r")
```


```python
first_line = file.readline()
```


```python
print(first_line)
```

    When you reach the end of your rope, tie a knot in it and hang on.
    
    


```python
file.close()
```


```python
file = open("quotes.txt", "r")
```


```python
lines = file.readlines()
```


```python
for line in lines:
    print(line)
```

    When you reach the end of your rope, tie a knot in it and hang on.
    
    Franklin D. Roosevelt
    
    Always remember that you are absolutely unique. Just like everyone else.
    
    Margaret Mead
    
    The best and most beautiful things in the world cannot be seen or even touched â€” they must be felt with the heart.
    
    Helen Keller
    
    Success depends upon previous preparation, and without such preparation, there is sure to be failure.
    
    Confucius
    
    The journey of a thousand miles begins with one step.
    
    Lao Tzu
    


```python
file.close()
```


```python
s1 = "Yeah, we fancy like Applebee's on a date night"
s2 = "Got that Bourbon Street steak with the Oreo shake"
s3 = "Get some whipped cream on the top too"
s4 = "Two straws, one check, girl, I got you"
```


```python
words_s1 = s1.split()
```


```python
print(words_s1[4])
```

    Applebee's
    


```python
words_s2 = s2.split()
```


```python
print(words_s2[-1])
```

    shake
    


```python
file = open("quotes.txt")
```


```python
lines = file.read()
```


```python
words = lines.split()
```


```python
num_words = len(words)
```


```python
print("The number of words is", num_words)
```

    The number of words is 85
    


```python
filepath
```




    'data\\summerDay.txt'




```python
file = open("quotes.txt", "r")
```


```python
lines = file.readlines()
```


```python
index_list = []
wordLength_list = []
toupled_list = []
i = 0
for line in lines:
    i += 1
    index_list.append(i)
    wordLength_list.append(len(line.split()))
    toupled_list.append([index_list[i - 1], wordLength_list[i - 1]])
    
    
    
```


```python
file.close()
```


```python

print(toupled_list)
```

    [[1, 16], [2, 3], [3, 11], [4, 2], [5, 23], [6, 2], [7, 15], [8, 1], [9, 10], [10, 2]]
    


```python
def numWordsPerLine(filepath):
    index_list = []
    wordLength_list = []
    filepath = []
    i = 0
    for line in lines:
        i += 1
        index_list.append(i)
        wordLength_list.append(len(line.split()))
        filepath.append([index_list[i - 1], wordLength_list[i - 1]])
    return filepath


```


```python
numWordsPerLine(file)
```




    [[1, 16],
     [2, 3],
     [3, 11],
     [4, 2],
     [5, 23],
     [6, 2],
     [7, 15],
     [8, 1],
     [9, 10],
     [10, 2]]




```python
import os 
datadir = "data"
```


```python
file = open("summerDay.txt", "r")
lines = file.readlines()
filepath = os.path.join(datadir, "summerDay.txt")
numWordsPerLine(filepath)

```




    [[1, 8],
     [2, 7],
     [3, 9],
     [4, 9],
     [5, 8],
     [6, 7],
     [7, 7],
     [8, 7],
     [9, 7],
     [10, 8],
     [11, 9],
     [12, 8],
     [13, 10],
     [14, 10]]




```python
file.close()
```


```python

```


```python

```

     Volume in drive C is OS
     Volume Serial Number is F802-CD04
    
     Directory of C:\Users\toddj\OneDrive - Dickinson College\Documents\GitHub\hw1-Toddthegod1\homeworks\hw1\data
    
    09/16/2024  09:09 PM    <DIR>          .
    09/16/2024  09:09 PM    <DIR>          ..
    09/16/2024  09:09 PM               112 babyNames.txt
    09/16/2024  10:53 PM               488 quotes.txt
    09/16/2024  09:09 PM               648 summerDay.txt
                   3 File(s)          1,248 bytes
                   2 Dir(s)  57,797,230,592 bytes free
    


```python

def readNamesCounts(filepath):
    namelist = []
    countlist = []
    ## FINISH THE FUNCTION HERE
    file = open("babyNames.txt", "r")
    for line in file:
        line = line.strip()
        count, name = line.split(',')
        countlist.append(int(count.strip()))
        namelist.append(name.strip())
    return namelist, countlist
        
filepath = os.path.join(datadir, "babyNames.txt")
namelist, countlist = readNamesCounts(filepath)
print(namelist)
print(countlist)
```

    ['Jacob', 'Ethan', 'Michael', 'Jayden', 'William', 'Alexander']
    [22127, 18002, 17350, 17179, 17051, 16756]
    


```python

```


```python

```
