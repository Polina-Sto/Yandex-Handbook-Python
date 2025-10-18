# Решения задач из хэндбука Яндекс «Основы Python»

### 4.3. Рекурсия. Декораторы. Генераторы

A. Рекурсивный сумматор
```python
def recursive_sum(*args):
    if not args:
        return 0
    return args[-1] + recursive_sum(*args[0:-1])
```
или
```python
def recursive_sum(*args):
    if not args:
        return 0
    return args[0] + recursive_sum(*args[1:])
```

B. Рекурсивный сумматор цифр
```python
def recursive_digit_sum(n):
    if not n:
        return 0
    return n % 10 + recursive_digit_sum(n // 10)
```

C. 
```python

```

D. Декор результата
```python
def answer(func):
    def wrap(*args, **kwargs):
        return f'Результат функции: {func(*args, **kwargs)}'
    return wrap
```

H. Генератор Фибоначчи
```python
def fibonacci(arg):
    n1 = 0
    n2 = 1
    for i in range(arg):
        yield n1
        n1, n2 = n2, n1 + n2
```

J. "Выпрямление" списка
```python
res = []


def make_linear(el):
    if type(el) is int:
        res.append(el)
    else:
        for i in el:
            if type(i) is list:
                make_linear(i)
            else:
                res.append(i)
    return res
```

