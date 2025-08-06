# Решения задач из хэндбука Яндекс «Основы Python»

### 2.1. Ввод и вывод данных. Операции с числами, строками. Форматирование

A. Привет, Яндекс!
```python
print("Привет, Яндекс!")
```

B. Привет, всем!
```python
user_name = input("Как Вас зовут?")
print("Привет,", user_name)
```

C. Излишняя автоматизация
```python
te = input()
print(te)
print(te)
print(te)
```

D. Сдача
```python
a = int(input())
b = 38 * 2.5
print(int(a - b))
```

E. Магазин
```python
a = int(input())
b = int(input())
c = int(input())
print(int(c - (a * b)))
```

F. Чек
```python
a = input()
b = int(input())
c = int(input())
d = int(input())
itog = b * c
sd = d - itog
print(f"""Чек 
{a} - {c}кг - {b}руб/кг 
Итого: {itog}руб
Внесено: {d}руб 
Сдача: {sd}руб
""")
```
