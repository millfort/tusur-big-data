# Корреляционный анализ в Python

## Результаты

Был получены слудующие тепловые карты корреляций.

Для женщин:

![corr heatmap for women](https://i.imgur.com/RnqMlHL.png)

Для мужчин:

![corr heatmap for men](https://i.imgur.com/YiEUPrs.png)

## Контрольные вопросы

1. Обратите внимание на диагональ слева направо в таблице корреляции. Почему диагональ заполнена единицами, это совпадение?
    
    Нет, это не совпадение😄. Она заполнена единицами, т.к. по диагонали располагается корреляция переменной с этой же переменной.

2. Можно видеть, также что значения в таблице являются зеркальными, значения ниже единичной диагонали имеют зеркальный аналог выше этой диагонали. Почему?

    Это так, потому что данная матрица является симметричной. Симметричные значение отражают корреляцию одной пары переменных.

3. Многие переменные пары представляют корреляцию, близкую к нулю. Что это обозначает?

    Чем ближе корреляция к нулю, тем больше это указывает на отсутствие связи между парой переменных.

4. Зачем было разделять данные по полу?

    Чтобы гарантировать, что результаты не будут искажены из-за различий в мужском и женском телах.

5. Какие переменные имеют более сильную корреляцию с размером мозга(`MRI_Count`)? Это ожидаемо?

    Для более точного ответа на этот вопрос лучше вывести значение корреляции в числовом значение, помимо цветового.

    Для женщин было получено следующее изображение:

    ![corr heatmap with values for women](https://i.imgur.com/GFA8aLR.png)

    Из этого изображения следует, что наибольшая корреляция наблюдается между размером мозга и весом, а также `PIQ` -- результат теста, который оценивает пространственные отношения, визуальную последовательность и другие визуальные перцептивные и зрительно-моторные навыки, в основном в невербальном формате.

    Для мужчин было получено следующиее изображение:

    ![corr heatmap with values for men](https://i.imgur.com/1xZcbDo.png)

    Из него следует, что что наибольшая корреляция наблюдается между размером мозга и всеми результатами тестов интелекта.

    Все эти выводы были неожиданными.