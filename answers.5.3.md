# Решения задач из хэндбука Яндекс «Основы Python»

### 5.3. Модель исключений Python. Try, except, else, finally. Модули

A. Обработка ошибок
```python
try:
    func()
except ValueError:
    print("ValueError")
except TypeError:
    print("TypeError")
except SystemError:
    print("SystemError")
else:
    print("No Exceptions")
```

B. Ломать — не строить
```python
try:
    func(None, "None")
except Exception:
    print("Ура! Ошибка!")
```

C. Ломать — не строить 2
```python
class Defective:

    def __repr__(self):
        raise Exception


try:
    func(Defective())
except Exception:
    print("Ура! Ошибка!")
```

D. Контроль параметров
```python
def only_positive_even_sum(a, b):
    try:
        if not (isinstance(a, int) and isinstance(b, int)):
            raise TypeError
        if a <= 0 or b <= 0:
            raise ValueError
        if a % 2 != 0 or b % 2 != 0:
            raise ValueError
    except TypeError:
        return 'Вызвано исключение TypeError'
    except ValueError:
        return 'Вызвано исключение ValueError'
    else:
        return a + b
```

G. Валидация имени
```python
import re


def name_validation(name):
    # li = 'абвгдеёжзийклмнопрстуфхцчшщуъэьюя'
    try:
        if type(name) is not str:
            raise TypeError
        if not re.fullmatch(r'[а-яА-ЯёЁ]+', name):
            raise CyrillicError
        if name[0].islower():
            raise CapitalError
        if any(ch.isupper() for ch in name[1:]):
            raise CapitalError   

    except TypeError:
        return 'Вызвано исключение TypeError'
    except CyrillicError:
        return 'Вызвано исключение CyrillicError'
    except CapitalError:
        return 'Вызвано исключение CapitalError'
    else:
        return name


class CyrillicError(Exception):
    pass


class CapitalError(Exception):
    pass
```

H. Валидация имени пользователя
```python
import re


def username_validation(name):
    try:
        if type(name) is not str:
            raise TypeError
        if not re.fullmatch(r'[a-zA-Z0-9_]+', name):
            raise BadCharacterError
        if re.match(r'[0-9]+', name):
            raise StartsWithDigitError

    except TypeError:
        return 'Вызвано исключение TypeError'
    except BadCharacterError:
        return 'Вызвано исключение BadCharacterError'
    except StartsWithDigitError:
        return 'Вызвано исключение StartsWithDigitError'
    else:
        return name


class BadCharacterError(Exception):
    pass


class StartsWithDigitError(Exception):
    pass
```
