# Решения задач из хэндбука Яндекс «Основы Python»

### 2.2. Условный оператор

A. Просто здравствуй, просто как дела
```python
pe = int(input())
va = int(input())
if pe > va:
    print("Петя")
else:
    print("Вася")
```

B. Кто быстрее?
```python
pe = int(input())
va = int(input())
to = int(input())
if pe > va and pe > to:
    print("Петя")
elif va > pe and va > to:
    print("Вася")
else:
    print("Толя")
```

C. Кто быстрее на этот раз?
```python
pe = int(input())
va = int(input())
to = int(input())
if pe > va and pe > to and va > to:
    print("""1. Петя
2. Вася
3. Толя""")
elif pe > va and pe > to and to > va:
    print("""1. Петя
2. Толя
3. Вася""")
elif va > pe and va > to and pe > to:
    print("""1. Вася
2. Петя
3. Толя""")
elif va > pe and va > to and to > pe:
    print("""1. Вася
2. Толя
3. Петя""")
elif to > pe and to > va and pe > va:
    print("""1. Толя
2. Петя
3. Вася""")
else:
    print("""1. Толя
2. Вася
3. Петя""")
```

D. Список победителей
```python
a = input()
b = input()
c = input()

print(min(a, b, c))
```

E. Яблоки
```python
# pe = 6 +n
# va = 12 +m
# to = -7
# ge = 2
# di = -n, -m
n = int(input())
m = int(input())
pe = 6 + n
va = 12 + m
if pe > va:
    print("Петя")
else:
    print("Вася")
```

F. Сила прокрастинации
```python
a = int(input())
if a % 4 == 0 and a != 1900:
    print("YES")
else:
    print("NO")
```

G. А роза упала на лапу Азора
```python
a = input()
b = input()
c = input()

print(min(a, b, c))
```

H. Зайка — 1
```python
dig = int(input())
d = dig % 10
c = (dig % 100 - d) / 10
b = (dig % 1000 - d - c * 10) / 100
a = dig // 1000

if a == d and b == c:
    print("YES")
else:
    print("NO")
```

I. Первому игроку приготовиться
```python
a = input()
b = input()
c = input()

print(min(a, b, c))
```

J. Лучшая защита — шифрование
```python
dig = int(input())
c = dig % 10
b = (dig % 100 - c) // 10
a = (dig - c - b * 10) // 100
su1 = b + c
su2 = a + b
if su1 >= su2:
    print(str(su1) + str(su2))
else:
    print(str(su2) + str(su1))
```

K. Красота спасёт мир
```python

```

L. Музыкальный инструмент
```python
a = int(input())
b = int(input())
c = int(input())
if (a + b) <= c or (a + c) <= b or (b + c) <= a:
    print('NO')
else:
    print('YES')
```

M. Властелин Чисел: Братство общей цифры
```python
a = int(input())
b = int(input())
c = int(input())
if a % 10 == b % 10 == c % 10:
    print(a % 10)
elif a // 10 == b // 10 == c // 10:
    print(a // 10)
```

N. Властелин Чисел: Две Башни
```python

```

O. Властелин Чисел: Возвращение Цезаря
```python

```

P. Легенды велогонок возвращаются: кто быстрее?
```python

```

Q. Корень зла
```python

```

R. Территория зла
```python

```
