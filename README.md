# Выбор кредита от Tinkoff.ru

Tinkoff.ru работает с сетью магазинов электроники, в которой присутствуют и другие банки. Заявка на кредит от покупателя поступает сразу в несколько банков, часть из них заявку одобряют. После этого покупатель выбирает, в каком банке кредит. Датасет содержит данные о кредитах на покупку электроники, которые были одобрены Tinkoff.ru. Необходимо предсказать, выберет ли покупатель кредит от Tinkoff.ru.

В credit_tinkoff.csv содержится 133200 строк с данными о клиентах сети магазинов электроники, в этих магазинах они подали заявки на кредит. Колонка open_account_flg содержит 1 если клиент выбрал Тинькофф и 0 в противном случае.

### С кодом проекта можно ознакомиться по [ссылке](/boost_tinkoff.ipynb).

## Предобработка данных

Предобработка данных включала в себя:
- обработку пропущенных значений;
- обработку категориальных признаков;
- приведение названий регионов к единому формату;
- стандартизацию числовых признаков. 

Также данные были проверены на баланс классов целевой переменной.

## Результирующие признаки

В результате работы была построена модель на основе XGBoost с площадью под ROC-кривой - 0.7694. Основными результирующими признаками были определены:
- Регион проживания
- Сумма кредита
- Внутренняя скоринговая оценка
- Месячный доход и возраст клиента

 ![tinkoff](https://github.com/user-attachments/assets/6fc7f65b-f08c-410a-8344-51b75d32ef5e)

При этом чаще всего кредит от Тинькофф выбирали жители таких регионов как Московская область, Москва, Краснодарский Край, Санкт-Петербург и Свердловская область.

![image](https://github.com/user-attachments/assets/d2eb9e8f-16cb-4977-96de-931eb45a29b1)

При этом потенциальные клиенты склоны отказываться от кредита при сумме свыше 80 тыс. руб.

![image](https://github.com/user-attachments/assets/e27dbeeb-f4e1-4735-97c9-6be6be333707)


P.S. Конкурс на лучшую модель проводился в рамках чемпионата на сайте [Boosters.pro](https://boosters.pro/championship/tinkoff1/overview).
