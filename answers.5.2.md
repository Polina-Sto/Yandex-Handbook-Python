# Решения задач из хэндбука Яндекс «Основы Python»

### 5.2. Волшебные методы, переопределение методов. Наследование

A. Классная точка 3.0
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


class PatchedPoint(Point):

    def __init__(self, *args):
        if not args:
            self.x, self.y = 0, 0
        elif len(args) == 1:
            self.x, self.y = args[0]
        else:
            self.x, self.y = args 
```

B. Классная точка 4.0
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


class PatchedPoint(Point):

    def __init__(self, *args):
        if not args:
            self.x, self.y = 0, 0
        elif len(args) == 1:
            self.x, self.y = args[0]
        else:
            self.x, self.y = args 

    def __str__(self):
        return f"({self.x}, {self.y})"

    def __repr__(self):
        return f"PatchedPoint({self.x}, {self.y})"
```

C. Классная точка 5.0
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


class PatchedPoint(Point):

    def __init__(self, *args):
        if not args:
            self.x, self.y = 0, 0
        elif len(args) == 1:
            self.x, self.y = args[0]
        else:
            self.x, self.y = args 

    def __str__(self):
        return f"({self.x}, {self.y})"

    def __repr__(self):
        return f"PatchedPoint({self.x}, {self.y})"

    def __add__(self, other):
        new_point = PatchedPoint(self.x, self.y)
        new_point.move(*other)
        return new_point

    def __iadd__(self, other):
        self.x += other[0]
        self.y += other[1]
        return self
```

D. Дроби v0.1
```python
import math


class Fraction:

    def __init__(self, *args):
        if type(args[0]) is str:
            if int(args[0].split('/')[0]) >= int(args[0].split('/')[1]) and \
               int(args[0].split('/')[0]) % int(args[0].split('/')[1]) == 0:
                self.x = round(int(args[0].split('/')[0]) / int(args[0].split('/')[1]))
                self.y = 1
            else:
                res = math.gcd(int(args[0].split('/')[0]), int(args[0].split('/')[1]))
                if res != 1:
                    self.x, self.y = int(int(args[0].split('/')[0]) / res), int(int(args[0].split('/')[1]) / res)
                else:
                    self.x, self.y = int(args[0].split('/')[0]), int(args[0].split('/')[1])
        elif len(args) == 1 and type(args) is str:
            self.x = args
            self.y = 1
        else:
            res = math.gcd(args[0], args[1])
            self.x, self.y = int(args[0] / res), int(args[1] / res)
        
    def numerator(self, number=None):
        if number is None:
            return self.x
        else:
            self.x = number
            res = math.gcd(self.x, self.y)
            self.x, self.y = int(self.x / res), int(self.y / res)

    def denominator(self, number=None):
        if number is None:
            return self.y
        else:
            self.y = number
            res = math.gcd(self.x, self.y)
            self.x, self.y = int(self.x / res), int(self.y / res)

    def __str__(self):
        return f"{self.x}/{self.y}"

    def __repr__(self):
        return f"Fraction({self.x}, {self.y})"
```


