# Решения задач из хэндбука Яндекс «Основы Python»

### 6.1. Модули math и numpy

A. Математика — круто, но это не точно
```python
import math

x = float(input())

part1 = math.log(math.pow(x, 3 / 16), 32)
part2 = math.pow(x, math.cos((math.pi * x) / (2 * math.e))) 
part3 = math.pow(math.sin(x / math.pi), 2)

res = part1 + part2 - part3
print(res)
```

B. Потоковый НОД
```python
import math
import sys


for row in sys.stdin:
    print(math.gcd(*map(int, row.split())))
```

C. Есть варианты?
```python
from math import comb

n, m = map(int, input().split())
print(m * comb(n, m) // n, comb(n, m))
```

D. Среднее не арифметическое
```python
import math


n = [*map(float, input().split())]
cou = len(n)

print(math.pow(math.prod(n), (1 / cou)))
```

E. Шаг навстречу
```python
import math


a = [*map(float, input().split())]
b = [*map(float, input().split())]

c = [b[0] * math.cos(b[1]), b[0] * math.sin(b[1])]

print(math.dist(a, c))
```

F. Матрица умножения
```python
import numpy as np


def multiplication_matrix(n):
    li = []
    for i in range(1, n + 1):
        li2 = []
        for p in range(1, n + 1):
            li2.append(p * i)
        li.append(li2)
    return np.array(li)
```

G. Шахматная подготовка
```python
import numpy as np


def make_board(n):
    li = np.zeros((n, n), dtype=np.int8)
    li[::2, ::2] = 1
    li[1::2, 1::2] = 1
    
    return np.array(li)
```

H. Числовая змейка 3.0
```python
import numpy as np


def snake(m, n, direction='H'):
    nu = np.arange(1, m * n + 1, dtype='int16')
    
    if direction == 'H':
        nu = nu.reshape(n, m)
        nu[1::2, ::] = nu[1::2, ::-1]
    else:
        nu = nu.reshape(m, n)
        nu[1::2, ::] = nu[1::2, ::-1]
        nu = nu.transpose()
         
    return nu
```

I. Вращение
```python
import numpy as np


def rotate(matrix, deg):
    for i in range(int(deg / 90)):
        matrix = np.rot90(matrix, -1)
    return matrix
```

J. Лесенка
```python

```
