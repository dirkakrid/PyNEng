## Функция filter

Функция filter() применяет функцию ко всем элементам последовательности, и возвращает те объекты, для которых функция вернула True.

Например, вернуть только те строки, в которых находятся числа:
```python
In [1]: list_of_strings = ['one', 'two', 'list', '', 'dict', '100', '1', '50']

In [2]: filter(str.isdigit, list_of_strings)
Out[2]: ['100', '1', '50']
```

Например, из списка чисел оставить только нечетные:
```python
In [3]: filter(lambda x: x%2, [10, 111, 102, 213, 314, 515])
Out[3]: [111, 213, 515]
```

Аналогично, только четные:
```python
In [4]: filter(lambda x: not x%2, [10, 111, 102, 213, 314, 515])
Out[4]: [10, 102, 314]
```

Из списка слов оставить только те, у которых количество букв больше двух:
```python
In [5]: list_of_words = ['one', 'two', 'list', '', 'dict']

In [6]: filter(lambda x: len(x) > 2, list_of_words)
Out[6]: ['one', 'two', 'list', 'dict']
```
