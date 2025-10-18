# Решения задач из хэндбука Яндекс «Основы Python»

### 4.2. Позиционные и именованные аргументы. Функции высших порядков. Лямбда-функции

A. Генератор списков
```python
def make_list(length, value=0):
    return [value] * length 
```

B. Генератор матриц
```python
def make_matrix(size, value=0):
    if str(size).isdigit():
        return [
            [value for i in range(size)]
            for i in range(size)
        ]
    else:
        shi = size[0]
        vi = size[1]
        return [
            [value for i in range(shi)]
            for i in range(vi)
        ]
```

C. 
```python

```

D. Имя of the month 2.0
```python
def month(num, mon='ru'):
    m = {
        'en': [
            'January', 'February', 'March',
            'April', 'May', 'June',
            'July', 'August', 'September',
            'October', 'November', 'December'
        ],
        'ru': [
            'Январь', 'Февраль', 'Март',
            'Апрель', 'Май', 'Июнь',
            'Июль', 'Август', 'Сентябрь',
            'Октябрь', 'Ноябрь', 'Декабрь'
        ]
    }
    if mon == 'ru':
        return m[mon][num - 1]
    else:
        return m[mon][num - 1]
```

E. Подготовка данных
```python
def to_string(*args, sep=' ', end='\n'):
    string = ''
    for el in args:
        string += str(el)
        if args.index(el) < len(args) - 1:
            string += sep 
    string += end
    return string
```

F. Арифметический помощник
```python
def get_operator(oper):
    if oper == '+':
        return sum_operator
    elif oper == '-':
        return min_operator
    elif oper == '*':
        return umn_operator
    elif oper == '//':
        return del_operator
    else:
        return step_operator


def sum_operator(a, b):
    return a + b


def min_operator(a, b):
    return a - b


def umn_operator(a, b):
    return a * b


def del_operator(a, b):
    return a // b

    
def step_operator(a, b):
    return a ** b
```

H. Странный рост
```python
def grow(*args, **kwargs):
    li = []
    plu = []
    for i in args:
        for el in kwargs:
            if i % len(el) == 0:
                plu.append(kwargs[el])
        for el in plu:
            i += el
        plu = []
        li.append(i)
    return tuple(li)
```

K. Кофейня
```python
nal = None


def order(*want):
    global nal
    if nal is None:
        nal = []
        nal.append(in_stock["coffee"])
        nal.append(in_stock['milk'])
        nal.append(in_stock['cream'])

    vidi = {"Эспрессо": (1, 0, 0), 
            "Капучино": (1, 3, 0), 
            "Макиато": (2, 1, 0), 
            "Кофе по-венски": (1, 0, 2), 
            "Латте Макиато": (1, 2, 1), 
            "Кон Панна": (1, 0, 1)}

    for i in want:
        if "Эспрессо" == i and vidi["Эспрессо"][0] <= nal[0]:
            nal[0] -= vidi["Эспрессо"][0]
            return 'Эспрессо'

        elif "Капучино" == i and vidi["Капучино"][0] <= nal[0] and vidi["Капучино"][1] <= nal[1]:
            nal[0] -= vidi["Капучино"][0]
            nal[1] -= vidi["Капучино"][1]
            return 'Капучино'

        elif "Макиато" == i and vidi["Макиато"][0] <= nal[0] and vidi["Макиато"][1] <= nal[1]:
            nal[0] -= vidi["Макиато"][0]
            nal[1] -= vidi["Макиато"][1]
            return 'Макиато'

        elif "Кофе по-венски" == i and vidi["Кофе по-венски"][0] <= nal[0] and vidi["Кофе по-венски"][2] <= nal[2]:
            nal[0] -= vidi["Кофе по-венски"][0]
            nal[2] -= vidi["Кофе по-венски"][2]
            return 'Кофе по-венски'

        elif "Латте Макиато" == i and vidi["Латте Макиато"][0] <= nal[0] and vidi["Латте Макиато"][1] <= nal[1]\
                and vidi["Латте Макиато"][2] <= nal[2]:
            nal[0] -= vidi["Латте Макиато"][0]
            nal[1] -= vidi["Латте Макиато"][1]
            nal[2] -= vidi["Латте Макиато"][2]
            return 'Латте Макиато'

        elif "Кон Панна" == i and vidi["Кон Панна"][0] <= nal[0] and vidi["Кон Панна"][2] <= nal[2]:
            nal[0] -= vidi["Кон Панна"][0]
            nal[2] -= vidi["Кон Панна"][2]
            return 'Кон Панна'

        else:
            if i == want[-1]:
                return 'К сожалению, не можем предложить Вам напиток'
```

L. В эфире рубрика «Эксперименты»
```python
chet = []
nechet = []


def enter_results(*args):
    global chet, nechet
    for i in args[::2]:
        chet.append(i) 
    for i in args[1::2]:
        nechet.append(i) 


def get_sum():
    global chet, nechet
    prom = 0
    prom2 = 0
    for i in chet:
        prom += i
    for i in nechet:
        prom2 += i
    return prom, prom2

    
def get_average():
    global chet, nechet
    prom = 0
    cou = 0
    prom2 = 0
    cou2 = 0
    for i in chet:
        prom += i
        cou += 1
    for i in nechet:
        prom2 += i
        cou2 += 1
    return round(prom / cou, 2), round(prom2 / cou2, 2)
```

M. Длинная сортировка
```python
lambda x: (len(x), x.lower())
```

P. Обратная связь
```python
def login(username, password, callback1, callback2):
    res = 0
    for i in str(username):
        res += ord(i)
    res *= len(username)
    if hex(res).upper()[:1:-1] == password:
        callback1(username)
    else:
        callback2(username)
```
