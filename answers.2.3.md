# Решения задач из хэндбука Яндекс «Основы Python»

### 2.3. Циклы

A. Раз, два, три! Ёлочка, гори!
```python
while (a := input()) != "Три!":
    print('Режим ожидания...')
print('Ёлочка, гори!')
```

B. Зайка — 3
```python
b = 0
while (a := input()) != "Приехали!":
    found = "зайка" in a
    if found is True:
        b += 1
print(b)
```

C. Считалочка
```python
a = int(input())
b = int(input())
for i in range(a, b + 1):
    print(i, end=" ")
```

D. Считалочка 2.0
```python
a = int(input())
b = int(input())
for i in range(a, b + 1):
    print(i, end=" ")
```

E. Внимание! Акция!
```python
b = 0
while (a := float(input())) != 0:
    if a >= 500:
        a *= 0.9
        b = b + a
    else:
        b = b + a
print(b)
```

F. НОД
```python
a = int(input())
b = int(input())
while a != 0 and b != 0:
    if a > b:
        a = a % b
    else:
        b = b % a
print(a + b)
```

G. НОК
```python

```

H. Излишняя автоматизация 2.0
```python
a = input()
b = int(input())
for i in range(b):
    print(a)
```

I. Факториал
```python
a = int(input())
b = 1
if a == 0:
    print(0)
else:
    for i in range(a):
        b *= a
        a -= 1
    print(b)
```

J. Маршрут построен
```python
c = 0
v = 0
u = 0 
z = 0
while (a := input()) != "СТОП":
    if a == "СЕВЕР":
        c += int(input())
    elif a == "ВОСТОК":
        v += int(input()) 
    elif a == "ЮГ":
        u += int(input()) 
    elif a == "ЗАПАД":
        z += int(input())
print(c - u)
print(v - z)
```

K. Цифровая сумма
```python
a = int(input())
x = 0
b = str(a)
for i in range(len(b)):
    x += a % 10
    a = a // 10
print(x)
```

L. Сильная цифра
```python
a = int(input())
x = 0
c = len(str(a))
for i in range(c):
    z = a % 10
    if z > x:
        x = z
    a = a // 10
print(x)
```

M. Первому игроку приготовиться 2.0
```python

```

N. Простая задача
```python
a = int(input())
x = 1
de = 0
for i in range(int(a**0.5 + 1)):
    if a % x == 0:
        de += 1
    x += 1
if de == 1 and a != 1:
    print('YES')
else: 
    print('NO')
```

O. Зайка - 4
```python
a = int(input())
res = 0
for i in range(a):
    b = input()
    if 'зайка' in b:
        res += 1
print(res)
```

P. А роза упала на лапу Азора 2.0
```python

```

Q. 
```python

```

R. 
```python

```
