# Решения задач из хэндбука Яндекс «Основы Python»

### 3.5. Потоковый ввод/вывод. Работа с текстовыми файлами. JSON

A. A+B+...
```python
from sys import stdin

lines = []
for line in stdin:
    lines.append((line.rstrip('\n').split()))

sum = 0
for i in lines:
    for e in i:
        sum += int(e)
print(sum)
```

B. Средний рост
```python
from sys import stdin

count = 0
sum = 0
text = stdin.readlines()
for i in text:
    i.rstrip('\n')
    e = i.split()
    num = int(e[2]) - int(e[1])
    count += 1
    sum += num

print(round(sum / count))
```

C. Без комментариев 2.0
```python
from sys import stdin
 
for line in stdin:
    code = line.rstrip('\n').split('#')[0]
    if code != '':
        print(code)
```

D. 
```python

```

E. А роза упала на лапу Азора 6.0
```python
from sys import stdin

lines = []
for line in stdin:
    lines.append(line.rstrip('\n'))
el = []
for i in lines:
    q = i.split()
    for e in q:
        if e.lower() == e.lower()[::-1]:
            el.append(e)

dop = []
for e in sorted(el):
    if e not in dop:
        print(e)
    dop.append(e)
```


L. Разделяй и властвуй
```python
a = input()
b = input()
c = input()
d = input()

ch = '24680'
nech = '13579'

with open(a, 'r') as file, open(b, 'w', encoding='UTF-8') as fileb, \
     open(c, 'w', encoding='UTF-8') as filec, open(d, 'w', encoding='UTF-8') as filed:
    for line in file:
        for el in line.split():
            ch1 = 0
            nech1 = 0
            for i in el:
                if i in ch:
                    ch1 += 1
                else:
                    nech1 += 1
            if ch1 > nech1:
                fileb.write(f'{el} ')
            elif ch1 < nech1:
                filec.write(f'{el} ')
            else:
                filed.write(f'{el} ')
        fileb.write('\n')
        filec.write('\n')
        filed.write('\n')
```
