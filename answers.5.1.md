# Решения задач из хэндбука Яндекс «Основы Python»

### 5.1. Объектная модель Python. Классы, поля и методы

A. Классная точка
```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y
```

B. Классная точка 2.0
```python
class Point:
    
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def move(self, new_x, new_y):
        self.x += new_x
        self.y += new_y
        return self.x, self.y

    def length(self, p):
        return round(((self.x - p.x) ** 2 + (self.y - p.y) ** 2) ** 0.5, 2)
```

C. Не нажимай красную кнопку!
```python
class RedButton:

    def __init__(self, ko=0):
        self.ko = ko

    def click(self):
        self.ko += 1
        print("Тревога!")

    def count(self):
        return self.ko
```

D. Работа не волк
```python
class Programmer:

    def __init__(self, name, pos='Junior'):
        self.name = name
        self.pos = pos
        self.ti = 0
        self.stav = 0
        self.zp = 0

    def work(self, time):
        salaries = {"Junior": 10, "Middle": 15, "Senior": 20}
        self.zp += time * (self.stav + salaries[self.pos])
        self.ti += time

    def rise(self):
        if self.pos == 'Junior':
            self.pos = 'Middle'
        elif self.pos == 'Middle':
            self.pos = 'Senior'
        elif self.pos == 'Senior':
            self.stav += 1

    def info(self):
        return f"{self.name} {self.ti}ч. {self.zp}тгр."
```

E. Классный прямоугольник
```python
class Rectangle:

    def __init__(self, x, y):
        self.x = x
        self.y = y

    def perimeter(self):   
        if self.x[0] >= self.y[0]:
            m = self.x[0] - self.y[0]
        else:
            m = self.y[0] - self.x[0]
        if self.x[1] >= self.y[1]:
            p = self.x[1] - self.y[1]
        else:
            p = self.y[1] - self.x[1]
        return round((m + p) * 2, 2)

    def area(self):
        if self.x[0] >= self.y[0]:
            m = self.x[0] - self.y[0]
        else:
            m = self.y[0] - self.x[0]
        if self.x[1] >= self.y[1]:
            p = self.x[1] - self.y[1]
        else:
            p = self.y[1] - self.x[1]
        return round(m * p, 2)
```

I. Очередь
```python
class Queue:
    def __init__(self):
        self.li = []

    def push(self, item):
        return self.li.append(item)

    def pop(self):
        return self.li.pop(0)

    def is_empty(self):
        if self.li == [] or self.li is None:
            return "is empty"   
```
