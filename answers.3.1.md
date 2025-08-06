# Решения задач из хэндбука Яндекс «Основы Python»

### 3.1. Строки, кортежи, списки

A. Азбука
```python
a = int(input())
for i in range(a):
    b = input()
    if b[0] == "а" or b[0] == "б" or b[0] == "в":
        c = True
    else:
        c = False
        break
if c is True:
    print('YES')
if c is False:
    print('NO')
```

B. Кручу-верчу
```python
a = input()
for i in a:
    print(i)
```

C. Анонс новости
```python
s = int(input())
n = int(input())
for i in range(n):
    za = input()
    if len(za) > s:
        print(f'{za[0:(s - 3)]}...')
    else:
        print(za)
```

D. Очистка данных
```python
b = []
while (a := str(input())) != "":
    if a[0] == "#" and a[-1] != "@":
        b.append(a.strip("#"))
    elif a[-1] == "@":
        pass
    else:
        b.append(a)

for i in b:
    print(i)
```

E. А роза упала на лапу Азора 4.0
```python
a = input()
b = list(a)
b.reverse()
c = list(a)
if c == b:
    print("YES")
else:
    print('NO')
```

F. Зайка — 6
```python
a = int(input())
b = 0
c = list()
for i in range(a):
    e = input()
    c.extend(e.split())
for i in c:
    if i == "зайка":
        b += 1
print(b) 
```

G. А и Б сидели на трубе
```python
a = input()
li = []
for i in a.split():
    li.append(i)
print(int(li[0]) + int(li[1]))
```

H. Зайка — 7
```python
a = int(input())
c = list()
for i in range(a):
    b = input()
    c.append(b)
for j in c:
    if j.find("зайка") != -1:
        print(j.find("зайка") + 1)
    else:
        print("Заек нет =(")
```

I. Без комментариев
```python

```

J. Частотный анализ на минималках
```python
b = list()
e = list()
big = 0
let = ''
while (a := input()) != "ФИНИШ":
    b.extend(a.lower())
for i in b:
    if i != ' ':
        e.append(i.lower())
e.sort()
for i in e:
    if e.count(i) > big:
        big = e.count(i)
        let = i
print(let)
```

K. Найдётся всё
```python

```

L. Меню питания
```python
a = int(input())
b = ["Манная", "Гречневая", "Пшённая", "Овсяная", "Рисовая"]
ind = 0
for i in range(a):
    if i % 5 == 0:
        ind += 1
    if i < len(b):
        print(b[i])
    elif i >= len(b):
        print(b[i - ind * 5])
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
