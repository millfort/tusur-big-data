# Измерение и анализ данных интернет-соединения с хранилищем данных в виду SQL базы данных

## Результаты

На основе полученных данных, изображенных на следующем рисунке, затруднительно сделать выводы о зависимости средней скорости интернет-подключения от населения района.

![print_from_csv('/tmp/rpi_data_test')](https://i.imgur.com/e0RdzgC.png)

Для лучшего отображения зависимости был построен **joinplot** отображающий среднюю скорость загрузки и население района. Из этого графика, приведенного ниже, можно сделать вывод, что существует прямая зависимость между скоростью загрузки и населением района.

![df_compact.head(3)](https://i.imgur.com/WRbR6fy.png)

## Контрольные вопросы

1. Что такое **csvsql**, как она работает?

    **csvsql** is a command-line utility which generate SQL statements for a CSV file or execute those statements directly on a database.

    В данном случая она использовалась для заполнения базы данных из csv файла.

2. Можно ли объединить таблицы в базе данных, как это сделать?

    Возможно. Для этого используется SQL-выражение **JOIN**, позволяющее скомбинировать строки из двух и более таблиц на основе связанного столбца между ними.

3. Какой метод Pandas позволяет добавлять информацию в базу данных?

    Это позволяет сделать метод `to_sql`, полное описание которого приведено в [документации](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_sql.html).

4. Что делает метод `fetchall()`?

    `fetchall()` fetches all the rows of a query result. It returns all the rows as a list of tuples. An empty list is returned if there is no record to fetch.

5. Почему для обработки данных используется библиотека Pandas, можно ли выполнить такую обработку другим способом?

    Pandas удобный и широкораспространенный инструмент, используемый для обработки данных. Он предоставляет множество функций для их обработки. Это, конечно, можно сделать и другими средствами, но такое решение будет более многословным, сложным и излишним.