# Решения задач из хэндбука Яндекс «Основы Python»

### 3.3. Списочные выражения. Модель памяти для типов языка Python

A. Список квадратов
```python
[number ** 2 for number in range(a, b + 1)]  
```

B. Список квадратов 2
```python
[i ** 2 for i in (range(a, b - 1, -1) if a > b else range(a, b + 1))]
```

C. Основы фильтрации
```python
[i for i in range(a, b + 1) if i % d == 0]
```

D. Множество нечетных чисел
```python
{el for el in numbers if el % 2 == 1}
```

E. Множество всех полных квадратов
```python
{el for el in numbers if el % (el ** 0.5) == 0}
```

F. Длины всех слов
```python
[len(i) for i in sentence.split()]
```

G. Цифровая выжимка
```python
''.join(map(str, [i for i in text if i in '0123456789']))
```

H. Аббревиатура
```python
''.join(i[0].upper() for i in string.split())
```

I. Преобразование в строку
```python
' - '.join(map(str, sorted([i for i in set(numbers)])))
```


```

R. 
```python

```
