# pr_06
# SQL для подготовки данных
### Цель:
Рассмотреть данные переписи населения США об использовании общественного транспорта относительно ZIP-кода.
Проанализировать, имеется ли корреляция между уровнем использования общественного транспорта с продажами в
организации в определенном регионе. Построить гистограмму распределения и диаграмму рассеяивания

1. Загружаем набор данных public_transportation_statistics_by_zip_code.csv с GitHub:
https://github.com/BosenkoTM/SQL-for-Begginer-DataAnalytics/blob/main/Datasets/public_transportation_statistics_by_zip_code.csv

2. Подключаем билеотеку psycopg2

![image](https://github.com/user-attachments/assets/ba379132-f54e-4b8a-8b1d-02cb356e4159)

3. Копируем данные public_transportation_statistics_by_zip_code.csv в базу данных клиентов организации, создав для них таблицу в наборе данных.

![image](https://github.com/user-attachments/assets/6c624335-b3d5-4b4e-997b-b8bb32c31844)

![image](https://github.com/user-attachments/assets/d4854d4f-12fc-4a90-8ac3-ebdc499628ce)

![image](https://github.com/user-attachments/assets/9c4a027b-90a8-4b34-a840-bb3d374bbd1f)

4. Найдем максимальное и минимальное процентное соотношение в данных. Значения ниже 0 принять как пустое значение

![image](https://github.com/user-attachments/assets/94d9fe98-a731-4c19-beca-5bae7ae13f26)

![image](https://github.com/user-attachments/assets/735e838e-2af5-4bf0-87ea-02ba13215a32)

5. Рассчитаем средний объем продаж для клиентов, проживающих в регионах с высоким уровнем использования общественного транспорта (более 10%), а также с низким уровнем использования общественного транспорта (менее или равным 10%)

![image](https://github.com/user-attachments/assets/6c377c6d-b3f9-4751-9d68-6814971c667a)

![image](https://github.com/user-attachments/assets/e2a35d09-5f27-4143-92ea-2807edaeb924)

6. Загрузим данные в pandas и построим гистограмму распределения(использовать my_data.plot.hist(y='public_transportation_pct') для построения гистограммы)

![image](https://github.com/user-attachments/assets/73154fe9-660a-4e16-9b95-64be5e302c16)

![image](https://github.com/user-attachments/assets/10ae8747-822d-43ae-8ad5-60863feebb59)

7. Сгруппируем клиентов по их zip_code, и посмотрим на среднее количество транзакций на одного клиента. Экспортируем эти данные в Excel и создадим диаграмму рассеяния, чтобы лучше понять взаимосвязь между использованием общественного транспорта и продажами

![image](https://github.com/user-attachments/assets/eaf302dd-504e-4cdd-ba58-d854c06a5359)

![image](https://github.com/user-attachments/assets/78020909-3206-48ea-a268-a82a768d61b3)

### Рекомендации возможностей расширения
Анализируя диаграмму рассеивания мы можем сделать вывод: чем больше людей пользуется общественным транспортом в районе, тем ниже средний объем продаж автомобилей и скутеров; максимальные продажи наблюдаются при минимальных использованиях общественного транспорта. Следовательно, основываясь на этих данных руководству компании следует открывать новые точки в местах с низкой долей людей, которые ездят на автобусах, метро и т.д.

### Вывод
Рассмотрели данные переписи населения США об использовании общественного транспорта относительно ZIP-кода.
Проанализировали, имеется ли корреляция между уровнем использования общественного транспорта с продажами в
организации в определенном регионе. Построили гистограмму распределения и диаграмму рассеяивания
