# Решения задач из хэндбука Яндекс «Основы Python»

### 6.2. Модуль pandas

A. Длины всех слов - 2
```python
import pandas as pd


def length_stats(text):
    text = "".join([x for x in text.lower() if x.isalpha() or x == " "])
    stats = pd.Series({x: len(x) for x in text.split()}).sort_index()
    return stats
```

B. Длины всех слов по чётности
```python
import pandas as pd


def length_stats(text):

    text = "".join([x for x in text.lower() if x.isalpha() or x == " "])
    odd = pd.Series({x: len(x) for x in text.split()}).sort_index()
    even = odd[odd % 2 == 0]
    odde = odd[odd % 2 != 0]

    return odde, even
```

C. Чек - 2
```python
import pandas as pd


def cheque(price_list, **purchases):
    m = {
        'product': list(purchases), 
        'price': [price_list[p] for p in purchases], 
        'number': list(purchases.values()), 
        'cost': [price_list[p] * n for p, n in purchases.items()]
    }
    df = pd.DataFrame(m)
    
    return df.sort_values('product').reset_index(drop=True)
```

D. Акция
```python
import pandas as pd


def cheque(price_list, **purchases):
    product = list(purchases)
    price = [price_list[p] for p in purchases]
    number = list(purchases.values())
    cost = [price_list[p] * n for p, n in purchases.items()]
    m = {
        'product': product, 
        'price': price, 
        'number': number, 
        'cost': cost
    }
    df = pd.DataFrame(m)
    
    return df.sort_values('product').reset_index(drop=True)


def discount(cheque):
    new = cheque.copy()
    new.loc[new['number'] > 2, 'cost'] = new['cost'] * 0.5
    return new.sort_values('product').reset_index(drop=True)
```

G. Отчёт неуспеваемости
```python
import pandas as pd


def need_to_work_better(journal):
    m = journal[(journal['maths'] == 2) | (journal['physics'] == 2) | (journal['computer science'] == 2)]
    return m
```

H. Обновление журнала
```python
import pandas as pd


def update(journal):
    average = journal.assign(average=lambda x: (x['maths'] + x['physics'] + x['computer science']) / 3)  
    return average.sort_values(['average', 'name'], ascending=[False, True])
```
