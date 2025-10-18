# Решения задач из хэндбука Яндекс «Основы Python»

### 3.4. Встроенные возможности по работе с коллекциями

A. Автоматизация списка
```python
f = input()
for index, value in enumerate(f.split(' '), 1):
    print(f'{index}. {value}')
```

B. Сборы на прогулку
```python
a = input()
b = input()
c = list(zip(a.split(', '), b.split(', ')))
for kids in c:
    print(f'{kids[0]} - {kids[1]}')
```

C. Рациональная считалочка
```python
from itertools import count

a = input()
er = a.split()
for i in count(float(er[0]), float(er[2])):
    if i <= float(er[1]):
        print(round(i, 2))
    else:
        break
```

D. Словарная ёлка
```python
from itertools import accumulate as acc

a = input()
b = a.split(' ')
c = list()
for i in b:
    c.append(i + ' ')

for el in acc(c):
    print(f"{el}  ")
```

E. Список покупок
```python
mom = input()
dad = input()
dau = input()

a = list()
for i in mom.split(', '):
    a.append(i)
for i in dad.split(', '):
    a.append(i)
for i in dau.split(', '):
    a.append(i)
a.sort()

for index, el in enumerate(a, 1):
    print(f'{index}. {el}')
```

F. Колода карт
```python
from itertools import product

a = input()

b = [2, 3, 4, 5, 6, 7, 8, 9, 10, 'валет', "дама", "король", "туз"]
c = ['пик', 'треф', 'бубен', 'червей']

for i in c:
    if a == i:
        c.remove(i)

for i in list(product(b, c)):
    print(f'{i[0]} {i[1]}')
```

G. Игровая сетка
```python
from itertools import combinations

a = int(input())
li = list()
for i in range(a):
    el = input()
    li.append(el)

for i in list(combinations(li, 2)):
    print(f'{i[0]} - {i[1]}')
```

H. 
```python

```

I. Таблица умножения 3.0
```python
from itertools import product, islice
a = int(input())
nums = range(1, a + 1)
table = [x * y for x, y in product(nums, repeat=2)]
for row in range(a):
    print(*islice(table, row * a, (row + 1) * a))
```
