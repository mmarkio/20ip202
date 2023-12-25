```python
#задание 0.
n = 27 
while True:
    print(n, end=' ')
    if n == 1:
        break
    if n %2:
        n = 3 * n + 1
    else:
        n=n//2
print()
```

    27 82 41 124 62 31 94 47 142 71 214 107 322 161 484 242 121 364 182 91 274 137 412 206 103 310 155 466 233 700 350 175 526 263 790 395 1186 593 1780 890 445 1336 668 334 167 502 251 754 377 1132 566 283 850 425 1276 638 319 958 479 1438 719 2158 1079 3238 1619 4858 2429 7288 3644 1822 911 2734 1367 4102 2051 6154 3077 9232 4616 2308 1154 577 1732 866 433 1300 650 325 976 488 244 122 61 184 92 46 23 70 35 106 53 160 80 40 20 10 5 16 8 4 2 1 
    


```python
for nn in range(1, 101):
    n, st = nn, 0
    while True:
        st+=1
        if n == 1:
            break
        if n %2:
            n = 3 * n + 1
        else:
            n = n //2
    print('st({}) = {}'.format(nn, st))
```

    st(1) = 1
    st(2) = 2
    st(3) = 8
    st(4) = 3
    st(5) = 6
    st(6) = 9
    st(7) = 17
    st(8) = 4
    st(9) = 20
    st(10) = 7
    st(11) = 15
    st(12) = 10
    st(13) = 10
    st(14) = 18
    st(15) = 18
    st(16) = 5
    st(17) = 13
    st(18) = 21
    st(19) = 21
    st(20) = 8
    st(21) = 8
    st(22) = 16
    st(23) = 16
    st(24) = 11
    st(25) = 24
    st(26) = 11
    st(27) = 112
    st(28) = 19
    st(29) = 19
    st(30) = 19
    st(31) = 107
    st(32) = 6
    st(33) = 27
    st(34) = 14
    st(35) = 14
    st(36) = 22
    st(37) = 22
    st(38) = 22
    st(39) = 35
    st(40) = 9
    st(41) = 110
    st(42) = 9
    st(43) = 30
    st(44) = 17
    st(45) = 17
    st(46) = 17
    st(47) = 105
    st(48) = 12
    st(49) = 25
    st(50) = 25
    st(51) = 25
    st(52) = 12
    st(53) = 12
    st(54) = 113
    st(55) = 113
    st(56) = 20
    st(57) = 33
    st(58) = 20
    st(59) = 33
    st(60) = 20
    st(61) = 20
    st(62) = 108
    st(63) = 108
    st(64) = 7
    st(65) = 28
    st(66) = 28
    st(67) = 28
    st(68) = 15
    st(69) = 15
    st(70) = 15
    st(71) = 103
    st(72) = 23
    st(73) = 116
    st(74) = 23
    st(75) = 15
    st(76) = 23
    st(77) = 23
    st(78) = 36
    st(79) = 36
    st(80) = 10
    st(81) = 23
    st(82) = 111
    st(83) = 111
    st(84) = 10
    st(85) = 10
    st(86) = 31
    st(87) = 31
    st(88) = 18
    st(89) = 31
    st(90) = 18
    st(91) = 93
    st(92) = 18
    st(93) = 18
    st(94) = 106
    st(95) = 106
    st(96) = 13
    st(97) = 119
    st(98) = 26
    st(99) = 26
    st(100) = 26
    


```python
#Задание 1.
import sys

try:
    n = int(sys.argv[1])
    if n < 1:
        raise ValueError
except (IndexError, ValueError):
    print('Введите целое число больше 0.\n'
          'for exmple, python {:s} 8'.format(sys.argv[0]))
    sys.exit(1)
    
while True:
    print(n, end=' ')
    if n == 1:
        break
    if n % 2:
        n = 3 * n + 1
    else:
        n = n // 2
print()
```

    ERROR:root:Internal Python error in the inspect module.
    Below is the traceback from this internal error.
    
    

    Введите целое число больше 0.
    for exmple, python C:\ProgramData\Anaconda3\lib\site-packages\ipykernel_launcher.py 8
    Traceback (most recent call last):
      File "<ipython-input-12-583e98b88f8b>", line 5, in <module>
        n = int(sys.argv[1])
    ValueError: invalid literal for int() with base 10: '-f'
    
    During handling of the above exception, another exception occurred:
    
    Traceback (most recent call last):
      File "C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\interactiveshell.py", line 3437, in run_code
        exec(code_obj, self.user_global_ns, self.user_ns)
      File "<ipython-input-12-583e98b88f8b>", line 11, in <module>
        sys.exit(1)
    SystemExit: 1
    
    During handling of the above exception, another exception occurred:
    
    Traceback (most recent call last):
      File "C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py", line 1101, in get_records
        return _fixed_getinnerframes(etb, number_of_lines_of_context, tb_offset)
      File "C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py", line 248, in wrapped
        return f(*args, **kwargs)
      File "C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py", line 281, in _fixed_getinnerframes
        records = fix_frame_records_filenames(inspect.getinnerframes(etb, context))
      File "C:\ProgramData\Anaconda3\lib\inspect.py", line 1515, in getinnerframes
        frameinfo = (tb.tb_frame,) + getframeinfo(tb, context)
    AttributeError: 'tuple' object has no attribute 'tb_frame'
    


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-12-583e98b88f8b> in <module>
          4 try:
    ----> 5     n = int(sys.argv[1])
          6     if n < 1:
    

    ValueError: invalid literal for int() with base 10: '-f'

    
    During handling of the above exception, another exception occurred:
    

    SystemExit                                Traceback (most recent call last)

        [... skipping hidden 1 frame]
    

    <ipython-input-12-583e98b88f8b> in <module>
         10           'for exmple, python {:s} 8'.format(sys.argv[0]))
    ---> 11     sys.exit(1)
         12 
    

    SystemExit: 1

    
    During handling of the above exception, another exception occurred:
    

    TypeError                                 Traceback (most recent call last)

        [... skipping hidden 1 frame]
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\interactiveshell.py in showtraceback(self, exc_tuple, filename, tb_offset, exception_only, running_compiled_code)
       2052                     stb = ['An exception has occurred, use %tb to see '
       2053                            'the full traceback.\n']
    -> 2054                     stb.extend(self.InteractiveTB.get_exception_only(etype,
       2055                                                                      value))
       2056                 else:
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in get_exception_only(self, etype, value)
        752         value : exception value
        753         """
    --> 754         return ListTB.structured_traceback(self, etype, value)
        755 
        756     def show_exception_only(self, etype, evalue):
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, evalue, etb, tb_offset, context)
        627             chained_exceptions_tb_offset = 0
        628             out_list = (
    --> 629                 self.structured_traceback(
        630                     etype, evalue, (etb, chained_exc_ids),
        631                     chained_exceptions_tb_offset, context)
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, value, tb, tb_offset, number_of_lines_of_context)
       1365         else:
       1366             self.tb = tb
    -> 1367         return FormattedTB.structured_traceback(
       1368             self, etype, value, tb, tb_offset, number_of_lines_of_context)
       1369 
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, value, tb, tb_offset, number_of_lines_of_context)
       1265         if mode in self.verbose_modes:
       1266             # Verbose modes need a full traceback
    -> 1267             return VerboseTB.structured_traceback(
       1268                 self, etype, value, tb, tb_offset, number_of_lines_of_context
       1269             )
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in structured_traceback(self, etype, evalue, etb, tb_offset, number_of_lines_of_context)
       1122         """Return a nice text document describing the traceback."""
       1123 
    -> 1124         formatted_exception = self.format_exception_as_a_whole(etype, evalue, etb, number_of_lines_of_context,
       1125                                                                tb_offset)
       1126 
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in format_exception_as_a_whole(self, etype, evalue, etb, number_of_lines_of_context, tb_offset)
       1080 
       1081 
    -> 1082         last_unique, recursion_repeat = find_recursion(orig_etype, evalue, records)
       1083 
       1084         frames = self.format_records(records, last_unique, recursion_repeat)
    

    C:\ProgramData\Anaconda3\lib\site-packages\IPython\core\ultratb.py in find_recursion(etype, value, records)
        380     # first frame (from in to out) that looks different.
        381     if not is_recursion_error(etype, value, records):
    --> 382         return len(records), 0
        383 
        384     # Select filename, lineno, func_name to track frames with
    

    TypeError: object of type 'NoneType' has no len()



```python
import sys
import math

haversin = lambda alpha: math.sin(alpha/2)**2
def gc_distance(loc1, loc2, R = 6378.1):
    
    (phi1, lambda1), (phi2, lambda2) = loc1, loc2
    d = 2 * R * math.asin(math.sqrt(haversin(phi2-phi1)
                + math.cos(phi1)*math.cos(phi2)*haversin(lambda2-lambda1)))
    return d
loc1, loc2 = sys.argv[1:]
phi1, lambda1 = [math.radians(float(x)) for x in loc1.split(',')]
phi2, lambda2 = [math.radians(float(x)) for x in loc2.split(',')]

d = gc_distance((phi1, lambda1), (phi2, lambda2))
print('{} km'.format(int(d)))
```


      File "<ipython-input-16-8b261805a0c3>", line 5
        def gc_distance(loc1, loc2,float R = 6378.1):
                                         ^
    SyntaxError: invalid syntax
    



```python

```
