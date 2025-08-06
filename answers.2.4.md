# Решения задач из хэндбука Яндекс «Основы Python»

### 2.4. Вложенные циклы

A. Таблица умножения
```python
a = int(input())
for i in range(1, a + 1): 
    for j in range(1, a + 1): 
        print(i * j, end=' ')
    print(" ")
```

B. Не таблица умножения
```python
a = int(input())
for i in range(1, a + 1): 
    for j in range(1, a + 1): 
        print(j, "*", i, "=", i * j, end="\n")
```

C. Новогоднее настроение
```python
max_num = int(input())
col = 1
num = 0

for i in range(1, max_num + 1):
    print(i, end=' ')
    num += 1
    if num == col:
        print()
        col += 1  
        num = 0  
```

D. Суммарная сумма
```python
a = int(input())
c = 0
for i in range(a):
    b = int(input())
    for j in str(b):
        c += int(j)
print(c)
```

E. Зайка — 5
```python
n = int(input())
s = 0
for i in range(1, n + 1):
    name = ''
    k = 0
    while name != 'ВСЁ': 
        name = input()
        if name == 'зайка':
            k += 1
    s += k > 0  
print(s)
```

F. 
```python

```

G. На старт! Внимание! Марш!
```python
a = int(input())
c = 3
for i in range(1, a + 1):
    for j in range(c, 0, -1):
        print(f"До старта {j} секунд(ы)")
    c += 1
    print(f"Старт {i}!!!")
```

H. Максимальная сумма
```python
a = int(input())
e = 0
res = None
for i in range(a):
    name = input()
    num = input()
    chisla = 0
    for i in num:
        chisla += int(i)
    if chisla >= e:
        res = name
        e = chisla
print(res)
```

I. Большое число
```python
a = int(input())
for i in range(a):
    num = input()
    maxi = 0
    for m in num:
        if int(m) > maxi:
            maxi = int(m)
    print(maxi, end='')
```

J. Мы делили апельсин
```python

```

K. 
```python

```

L. 
```python

```

M. 
```python

```

N. 
```python

```
O. 
```python

```

P. 
```python

```

Q. 
```python

```

R. 
```python

```
