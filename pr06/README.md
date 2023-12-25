```python
#Практическая работа №6
#Задание 0.
import numpy as np
import sys
import pylab

def parse_line(fi):
    fi.readline()
    fi.readline()
    rollover = False
    for line in fi:
        fields = line.split()
        nwinners = int(fields[6])
        if nwinners == 0:
            rollover = True
            continue
        if rollover:
            rollover = False
            continue
        balls = np.array([int(v) for v in fields[:6]])
        jackpot_share = float(fields[7])
        nlow = sum(balls < 13)
        yield nlow, jackpot_share
        
with open('lottery-draws.txt') as fi:
    data = list(parse_line(fi))
    
data = np.array(data)

print(np.corrcoef(data, rowvar=0))
```

    [[ 1.         -0.19909853]
     [-0.19909853  1.        ]]
    


```python
#Задание 1.
marks = np.array([3, 5, 14, 22, 30, 44, 7])
bins = [0, 20, 40, 60, 80, 100]
hist, bins = np.histogram(marks, bins)

print(bins)

bin_centres = (bins[:-1] + bins[1:])/2
print(bin_centres)

import matplotlib.pyplot as plt

plt.bar(bin_centres, hist, width=10, align='center')
```

    [  0  20  40  60  80 100]
    [10. 30. 50. 70. 90.]
    




    <BarContainer object of 5 artists>




    
![png](output_1_2.png)
    



```python
fsample = np.loadtxt('ex6-3-f-female-heights.txt').flatten()
msample = np.loadtxt('ex6-3-f-male-heights.txt').flatten()
heights = np.zeros((1000,), dtype={'names': ['female', 'male'], 'formats': ['f8', 'f8']})
heights['female'] = np.loadtxt('ex6-3-f-female-heights.txt').flatten()
heights['male'] = np.loadtxt('ex6-3-f-male-heights.txt').flatten()
fav, fstd = heights['female'].mean(), heights['female'].std()
mav, mstd = heights['male'].mean(), heights['male'].std()
all_heights_view = heights.view((('f8', 2))).flatten()
all_heights.min(), all_heights.max()
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-4-2ef1d68a53c1> in <module>
          7 mav, mstd = heights['male'].mean(), heights['male'].std()
          8 all_heights_view = heights.view((('f8', 2))).flatten()
    ----> 9 all_heights.min(), all_heights.max()
    

    NameError: name 'all_heights' is not defined



```python

```
