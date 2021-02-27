# Измерение и анализ данных интернет-соединения

## Результаты

### Вывод `print_from_csv('/tmp/rpi_data_test')`:
![print_from_csv('/tmp/rpi_data_test')](https://i.imgur.com/irRQRD2.png)
### Вывод `df_compact.head(3)`:
![df_compact.head(3)](https://i.imgur.com/lXn7O2V.png)

## Контрольные вопросы

1. Что такое анонимная функция в Python, как она работает

    In Python, an anonymous function, also known as lambda function, is a function that is defined without a name. A lambda function in python has the following syntax: 
    ```
    lambda arguments: expression
    ```
    Lambda functions can have any number of arguments but only one expression. The expression is evaluated and returned. Lambda functions can be used wherever function objects are required.

2. Что возвращает функция `speedtest()`? Какой код используется для просмотра результатов функции `speedtest()`?
    
    Code:
    ```python
    st = speedtest()
    print(st, type(st))
    ```
    Result:
    ```
    [b'Ping:', b'51.674', b'ms', b'Download:', b'68.11', b'Mbit/s', b'Upload:', b'77.07', b'Mbit/s', '2021-02-27 12:35:09'] <class 'list'>
    ```

3. Каким образом выполняется переименнование столбцов датафрейма?

    С помощью функции `rename`, описание которой можно найти в [документации](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.rename.html). 
    
    Пример переименования столбца `Measure A` в `Ping (ms)` в датасете `df_compact`:
    ```python
    df_compact.rename(columns={'Measure A': 'Ping (ms)'}, inplace=True)
    ```

4. Для чего в лабораторной работе импортируется библиотека NumPy?

    Numpy is a library that adds support for large, multi-dimensional array and matrices along with high-level math functions to operate on these arrays. Pandas is built on numpy, and probably you often will create an array using numpy which is then passed to pandas. But it's not necessary to import numpy in the lab.

5. Как выглядит код удаления столбца Datetime?

    ```python
    df_compact.drop('Datetime', axis=1, inplace=True)
    ```

