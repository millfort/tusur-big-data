# Преступления в Сан-Франциско

## Результаты

Получившияся карта, на которой кругами отмечены преступления, цвет каждого из которых принадлежит определенному округу:
![result image](https://i.imgur.com/CQUF2nL.png)

## Контрольные вопросы

1. Сколько всего административных округов в Сан-Франциско?
    
    Code:
    ```python
    print('Количесво административных округов =', len(np.unique(SF['PdDistrict'])))
    ```
    Result:
    ```
    Количесво административных округов = 10
    ```

1. В каких административных округах наибольшая преступность?
    
    Code:
    ```python
    print('Количество преступлений по округам в порядке убывания:\n')
    print(SF['PdDistrict'].value_counts())
    ```
    Result:
    ```
    Количество преступлений по округам в порядке убывания:

    SOUTHERN      6185
    MISSION       4011
    CENTRAL       3867
    NORTHERN      3205
    BAYVIEW       2970
    INGLESIDE     2613
    TENDERLOIN    2449
    TARAVAL       2038
    PARK          1800
    RICHMOND      1622
    ```

1. Какие виды преступлений совершаются чаще всего?
    
    Code:
    ```python
    print('Количество преступлений по типу в порядке убывания:\n')
    print(SF['Category'].value_counts()))
    ```
    Result:
    ```python
    Количество преступлений по типу в порядке убывания:

    LARCENY/THEFT                 8205
    OTHER OFFENSES                4004
    NON-CRIMINAL                  3653
    ASSAULT                       2518
    VEHICLE THEFT                 1885
                                ... 
    SEX OFFENSES, NON FORCIBLE       5
    BAD CHECKS                       3
    GAMBLING                         1
    BRIBERY                          1
    PORNOGRAPHY/OBSCENE MAT          1
    ```

1. Каково назначение функции Лямбда в Python?
    
    In Python, a lambda function is a single-line function declared with no name, which can have any number of arguments, but it can only have one expression

1. Какие виды преступлений регистрируются в Сан-Франциско?
    
    Code:
    ```python
    print('Виды преступлений, которые регистрируются в Сан-Франкциско:')
    print('\n'.join(np.unique(SF['Category'])))
    ```
    Result:
    ```
    Виды преступлений, которые регистрируются в Сан-Франкциско:
    ARSON
    ASSAULT
    BAD CHECKS
    BRIBERY
    BURGLARY
    DISORDERLY CONDUCT
    DRIVING UNDER THE INFLUENCE
    DRUG/NARCOTIC
    DRUNKENNESS
    EMBEZZLEMENT
    EXTORTION
    FAMILY OFFENSES
    FORGERY/COUNTERFEITING
    FRAUD
    GAMBLING
    KIDNAPPING
    LARCENY/THEFT
    LIQUOR LAWS
    LOITERING
    MISSING PERSON
    NON-CRIMINAL
    OTHER OFFENSES
    PORNOGRAPHY/OBSCENE MAT
    PROSTITUTION
    ROBBERY
    RUNAWAY
    SEX OFFENSES, FORCIBLE
    SEX OFFENSES, NON FORCIBLE
    STOLEN PROPERTY
    SUICIDE
    SUSPICIOUS OCC
    TRESPASS
    VANDALISM
    VEHICLE THEFT
    WARRANTS
    WEAPON LAWS
    ```