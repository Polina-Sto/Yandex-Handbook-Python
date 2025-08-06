# Решения задач из хэндбука Яндекс «Основы Python»

### 3.2. Множества, словари

A. Символическая выжимка
```python
a = input()
b = set(a)
print(''.join(b))
```

B. Символическая разница
```python
a = input()
b = input()
c = set(a)
d = set(b)
print(''.join(c & d))
```

C. Зайка — 8
```python
a = int(input())
b = dict()
num = 0
for i in range(a):
    c = input()
    for j in c.split():
        if j not in b:
            b[j] = [num]
        else:
            b[j].append(num)
    num += 1
for key in b.keys():
    print(key)
```

D. Кашееды
```python
man = int(input())
ovs = int(input())
fam = dict()
for i in range(man):
    a = input()
    if a not in fam:
        fam[a] = ["man"]

for j in range(ovs):
    b = input()
    if b not in fam:
        fam[b] = ["ovs"]
    else:
        fam[b].append("ovs")

cou = 0    
for value in fam.values():
    if value == ["man", "ovs"]:
        cou += 1
if cou > 0:
    print(cou)
else:
    print("Таких нет")
```

E. Кашееды — 2
```python
man = int(input())
ovs = int(input())
fam = dict()
for i in range(man + ovs):
    a = input()
    if a not in fam:
        fam[a] = ["man"]
    else:
        fam[a] = ["ovs"]
cou = 0
for value in fam.values():
    if value == ["man"]:
        cou += 1
if cou > 0:
    print(cou)
else:
    print("Таких нет")
```

F. Кашееды — 3
```python
man = int(input())
ovs = int(input())
fam = dict()
for i in range(man + ovs):
    a = input()
    if a not in fam:
        fam[a] = ["man"]
    else:
        fam[a].append("ovs")
cou = 0
fams = []   
for key, value in fam.items():
    if value != ["man", "ovs"]:
        fams.append(key)
        cou += 1
if cou == 0:
    print("Таких нет")
else:    
    fams.sort()
    for e in fams:
        print(e)
```

G. Азбука Морзе
```python
a = input()
morze = {'a': '.-', 'b': '-...', 'c': '-.-.', 'd': '-..',   
         'e': '.', 'f': '..-.', 'g': '--.', 'h': '....',
         'i': '..', 'j': '.---', 'k': '-.-', 'l': '.-..',
         'm': '--', 'n': '-.', 'o': '---', 'p': '.--.',
         'q': '--.-', 'r': '.-.', 's': '...', 't': '-',
         'u': '..-', 'v': '...-', 'w': '.--', 'x': '-..-',
         'y': '-.--', 'z': '--..', ' ': '\n'}


for i in a.lower():
    if i == ' ':
        print()
    else:
        print(morze[i], end=' ')
```

H. Кашееды — 4
```python

```

I. Зайка — 9
```python
slova = {}
while (line := input()) != "":
    for i in line.split():
        slova[i] = slova.get(i, 0) + 1
for slovo, nums in slova.items():
    print(f'{slovo} {nums}')
```

J. Транслитерация
```python
a = input()

symb = {'А': 'A', 'Б': 'B', 'В': 'V', 'Г': 'G', 'Д': 'D', 'Е': 'E',
        'Ё': 'E', 'Ж': 'Zh', 'З': 'Z', 'И': 'I', 'Й': 'I', 'К': 'K',
        'Л': 'L', 'М': 'M', 'Н': 'N', 'О': 'O', 'П': 'P', 'Р': 'R',
        'С': 'S', 'Т': 'T', 'У': 'U', 'Ф': 'F', 'Х': 'Kh',
        'Ц': 'Tc', 'Ч': 'Ch', 'Ш': 'Sh', 'Щ': 'Shch', 'Ы': 'Y',
        'Э': 'E', 'Ю': 'Iu', 'Я': 'Ia'}

for i in a:
    if i.isupper() and i.upper() in symb:
        print(symb[i.upper()], end='')
    elif i.islower() and i.upper() in symb:
        print(symb[i.upper()].lower(), end='')
    elif i == 'ь' or i == 'ъ' or i == 'Ъ' or i == 'Ь':
        continue
    else:
        print(i, end='')
```

K. Однофамильцы
```python
a = int(input())
di = {}
res = 0
for i in range(a):
    m = input()
    if m not in di:
        di[m] = 1
    else:
        di[m] += 1
for i in di.values():
    if i > 1:
        res += i
print(res)
```

L. Однофамильцы — 2
```python

```

M. Дайте чего-нибудь новенького!
```python
n = int(input())
can = []
was = []
res = []
for i in range(n):
    can.append(input())
m = int(input())
for i in range(m):
    c = int(input())
    for i in range(c):
        was.append(input())

was_set = set(was)
can_set = set(can)

res = can_set - was_set

if len(res) == 0:
    print('Готовить нечего')
else:
    for i in sorted(res):
        print(i)
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
