# Решения задач из хэндбука Яндекс «Основы Python»

### 4.1. Функции. Области видимости. Передача параметров в функции

A. Функциональное приветствие
```python
def print_hello(name):
    print(f'Hello, {name}!')
```

B. Функциональный НОД
```python
def gcd(a, b):
    while a != 0 and b != 0:
        if a > b:
            a = a % b
        else:
            b = b % a
    return a + b
```

C. Длина числа
```python
def number_length(num):
    a = str(num)
    if a[0] == "-":
        return len(a) - 1
    return len(a)
```

D. Копейка рубль бережёт
```python
def take_small(money):
    res = []
    for el in money:
        if el < 100:
            res.append(el)
    return res
```

E. Виртуальный кликер
```python
schet = 0


def click():
    global schet
    schet += 1


def get_count():
    global schet
    return schet
```

F. Странная игра
```python
schet = 0


def move(player, number):
    global schet
    if player == 'Петя':
        schet += number
    if player == 'Ваня':
        schet -= number


def game_over():
    global schet
    if schet > 0:
        return 'Петя'
    elif schet < 0:
        return 'Ваня'
    else:
        return 'Ничья'
```

G. Максимальный максимум
```python
def max2D(matrix):
    res = 0
    for i in matrix:
        for el in i:
            if el > res:
                res = el
    return res
```

H. Числовое фрагментирование
```python
def fragments(numbers):
    res = []
    mini = []
    sred = -100000000
    for el in numbers:
        if el < sred:
            res.append(mini)
            mini = []
        mini.append(el)
        sred = el
    res.append(mini)
    return res
```

I. Имя of the month
```python
def month(number, language):
    MONTH = {
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
    return MONTH[language][number - 1]
```

J. Числовая строка
```python
def split_numbers(text):
    m = []
    for i in text.split():
        m.append(int(i))
    tu = tuple(m)
    return tu
```


