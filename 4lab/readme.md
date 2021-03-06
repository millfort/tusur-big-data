# Описательная статистика в Python

## Результаты

Был получен следующий частотный график значений:

![value frequency plot](https://i.imgur.com/UBjMeLn.png)

## Контрольные вопросы

1. Какие статистические значения для датафрейма позволяет получить метод `describe()`?
    
    Он позволяет получить:
    * количество записей(`count`),
    * среднее значение(`mean`),
    * среднеквадратическое отклонение(`std`),
    * минимальное значение(`min`),
    * .25, .50 и .75 перцентили(`25%`, `50%`, `75%`),
    * максимальное значение(`max`).

    Для текущего датасета данный метод выводит следующие статистики:

    ![example describe() output](https://i.imgur.com/BcfhcxV.png)

2. Как добавить в датафрейм новый столбец с данными?

     Для создания нового столбца используется имя нового столбца в кавычках в квадратных скобках в качестве индекса для кадра данных.

     Например:
     ```python
     data['rounded'] = data.weight.round(2)
     ```

3. Что такое частотное распределение данных?

    Это объект типа "серия данных", в котором столбец индекса задается уникальными значениеми данных, а другой столбец показывает число появлений соответсвующего значения.

4. Что делает функция `to_frame()` и почему необходимо преобразовать серию данных в датафрейм?

    Она преобразовывает серию данных в датафрейм. Это необходимо, чтобы работать с этими данными как с датафреймом.

5. Как при выводе значения переменной в текстовой строке оставить только 2 цифры после десятичной точки, если исходной значение содержит больше цифр.

    Для этого необходимо применить следующее форматирование:
    ```python
    f'{value:.2f}'
    ```

    Например:
    ```python
    a = 123.456789
    print(f'a = {a:.2f}') # a = 123.46
    ```


    