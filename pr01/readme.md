Практическая работа 1
```python
list = [2, 4, 10, 6, 8, 4]
minN = min(list)
maxN = max(list)

for i in range(len(list)):
    list[i] = (list[i] - minN) / (maxN - minN)
    
print(list)
```

    [0.0, 0.25, 1.0, 0.5, 0.75, 0.25]
    


```python
import math
a = 3.
b = 5.
while a != b:
    a, b = (a + b) / 2, math.sqrt(a * b)
    
print(a)
```

    3.9362355036495558
    


```python
import math
a = 1.
b = math.sqrt(2.)
while a != b:
    a, b = (a + b) / 2, math.sqrt(a * b)
    
print(1/a)
```

    0.8346268416740731
    


```python
for i in range(100):
    if i % 3 == 0 and i % 5 == 0:
        print(i, ': FizzBuzz')
    elif i % 5 == 0:
        print(i, ': Buzz')
    elif i % 3 == 0:
        print(i, ': Fizz')
```

    0 : FizzBuzz
    3 : Fizz
    5 : Buzz
    6 : Fizz
    9 : Fizz
    10 : Buzz
    12 : Fizz
    15 : FizzBuzz
    18 : Fizz
    20 : Buzz
    21 : Fizz
    24 : Fizz
    25 : Buzz
    27 : Fizz
    30 : FizzBuzz
    33 : Fizz
    35 : Buzz
    36 : Fizz
    39 : Fizz
    40 : Buzz
    42 : Fizz
    45 : FizzBuzz
    48 : Fizz
    50 : Buzz
    51 : Fizz
    54 : Fizz
    55 : Buzz
    57 : Fizz
    60 : FizzBuzz
    63 : Fizz
    65 : Buzz
    66 : Fizz
    69 : Fizz
    70 : Buzz
    72 : Fizz
    75 : FizzBuzz
    78 : Fizz
    80 : Buzz
    81 : Fizz
    84 : Fizz
    85 : Buzz
    87 : Fizz
    90 : FizzBuzz
    93 : Fizz
    95 : Buzz
    96 : Fizz
    99 : Fizz
    


```python
a = int(input())

if a == 1:
    str = 'CH2-CH2'
else:
    str = 'H3C'
    a -= 1
while a != 0:
    if a - 1 != 0:
        str += '-CH2'
    else:
        str += '-CH3'
    a -= 1
    
print(str)
```

    1
    CH2-CH2-CH3
    


```python

```
