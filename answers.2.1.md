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

G. Делу — время, потехе — час
```python
a = 'Купи слона!'
b = int(input())
i = 0
while i < b:
    i += 1
    print(a)
```

H. Наказание
```python
a = int(input())
b = input()
i = 0
while i < a:
    i += 1
    print(f'Я больше никогда не буду писать "{b}"!')
```

I. Деловая колбаса
```python
t = int(input())
deti = int(input())
time = 2
q = t / time
itog = q * deti
print(int(itog))
```

J. Детский сад — штаны на лямках
```python
name = input()
a = int(input())
b = a % 10
c = int((a % 100 - b) / 10)
e = a % 100
d = int((a - b - c * 10) / 100)

print(f'''Группа №{d}.
{b}. {name}.
Шкафчик: {a}.
Кроватка: {c}.
''')
```

K. Автоматизация игры
```python
dig = int(input())
d = int(dig % 10)
c = int((dig % 100 - d) / 10)
b = int((dig % 1000 - d - c * 10) / 100)
a = int(dig // 1000)

print(b, a, d, c, sep="")
```

L. Интересное сложение
```python
a = int(input())
b = int(input())
ed1 = a % 10
ed2 = b % 10
dec1 = (a % 100 - ed1) // 10
dec2 = (b % 100 - ed2) // 10
sot1 = a // 100
sot2 = b // 100

res1 = (ed1 + ed2) % 10
res2 = (dec1 + dec2) % 10
res_sot = (sot1 + sot2) % 10

print(f'{res_sot}{res2}{res1}')
```

M. Дед Мороз и конфеты
```python
a = int(input())
b = int(input())
res1 = b // a
res2 = b % a
print(res1)
print(res2)
```

N. Шарики и ручки
```python
k = int(input())
z = int(input())
s = int(input())

print(k + s + 1)
```
O. В ожидании доставки
```python
ch = int(input())
mi = int(input())
t = int(input())

if mi + (t % 60) >= 60:
    mi_res = mi + (t % 60) - 60
    ch_res = (ch + (t // 60) + 1) % 24
else:
    ch_res = (ch + (t // 60)) % 24
    mi_res = mi + (t % 60)

if ch_res < 10 and mi_res < 10:
    print(f'0{ch_res}:0{mi_res}')
elif ch_res < 10:
    print(f'0{ch_res}:{mi_res}')
elif mi_res < 10:
    print(f'{ch_res}:0{mi_res}')
else:
    print(f'{ch_res}:{mi_res}')
```

P. Доставка
```python
sklad = int(input())
shop = int(input())
s = int(input())

res = (shop - sklad) / s
print(round(res, 2))
```

Q. Ошибка кассового аппарата
```python
su = int(input())
last = int(input(), 2)

print(su + last)
```

R. Сдача 10
```python
check = int(input(), 2)
money = int(input())

print(money - check)
```
