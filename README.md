В нашем распоряжении датасет, содержащий информацию о клиентах банка «Метанпром». Банк располагается в Ярославле и областных городах: Ростов Великий и Рыбинск.
 
**ЗАДАЧИ ПРОЕКТА**

Проанализируйте клиентов регионального банка и выделите сегменты клиентов,
которые склонны уходить из банка.

- Проведите исследовательский анализ данных, определите все значимыепризнаки отточности (интервалы значений характеристик, которые связаны сповышенным оттоком, сравните портреты типичных клиентов, которыесклонны и не склонны уходить из банка и т.д)

- Сформулируйте и проверьте статистические гипотезы.

Проверьте гипотезу различия дохода между теми клиентами, которые
ушли и теми, которые остались.

Сформулируйте и проверьте статистическую гипотезу относительно
представленных данных, которая поможет внести ясность в исследование

- Объединяя признаки отточности, сформируйте сегменты, отберите из них лучшие и дайте по ним рекомендации

**ЦЕЛЬ ПРОЕКТА**

Проанализировать клиентов регионального банка и выделить сегменты клиентов, которые склонны уходить из банка

**Описание датасета**

/datasets/bank_scrooge.csv

Колонки:
- USERID — идентификатор пользователя,
- score — баллы кредитного скоринга,
- city — город,
- gender — пол,
- age — возраст,
- equity — количество баллов собственности
- balance — баланс на счёте,
- products — количество продуктов, которыми пользуется клиент,
- credit_card — есть ли кредитная карта,
- last_activity — активный клиент,
- EST_SALARY — оценочный доход клиента,
- сhurn — признак оттока.

**ВЫВОДЫ**

 Проведенное исследование показало, что между оттоком клиентов и некоторыми параметрами существует устойчивая корреляция, тогда как другие параметры практически не влияют на отток.
К параметрам, влияющим на отток, относятся:
- оценка объектов собственности клиента: чем выше оценка собственности, тем больше процент отточных клиентов;
- скоринговый рейтинг клиента: из банка уходили клиенты со скоринговым баллом не ниже 825, а клиенты с более высоким скоринговым рейтингом показывали более высокий процент оттока;
-количество продуктов, которыми пользуется клиент: клиенты, использовавшие 4 продукта, уходили из банка намного чаще, чем другие;
- вность пользователя: более активные клиенты покидали банк чаще, чем менее активные;
-пол пользователя: мужчины намного сильнее склонны уходить из банка, чем женщины;

Выявили интервалы значений характеристик, которые связаны с повышенным оттоком, это:
- баллы кредитного скоринга в диапазоне от 825 до 940;
- возраст от 25 до 35, от 48 до 60;
- баланс на счёте от 800 тыс. до 35 000 000 скорее всего это связано с переходом из регионального в более крупный банк;
- оценочный доход клиента от 100 тыс. до 200 тыс..
Портрет склонного к уходу клиента:
- склонные к уходу жители Ярославля,
- мужского пола,
- без кредитной карты и достаточно активный.
Мы провели сегментацию двумя способами  сегментами где Первый сегмент мы включили признаки оттока клиентов не учитывая возраст, во второй мы выбрали группу с признаками надежности клиента, и в третью это клиенты по портрету оттока, также учитывая что у нас есть фактически готовые сегменты, провели сегментацию клиентов на основе данных о количестве потребляемых продуктов.
В первом случае сегментация была проведена скорее для выявления слабых сторон и естественно сегмент с лучшими характеристиками это:
Второй сегмент:
- Пол:  любой
- Возраст: от 35 до 48
- Город: любой
- Оценка объектов собственности: до 5 
- Скоринговый рейтинг: до 825 и от 940
- Количество используемых продуктов: до 3
- Наличие кредитной карты: неважно
- Пользовательская активность: неважно
-  Оценочный доход: от 200000

с :
- Размер второго сегмента: 577
- Число отточных клиентов в первом сегменте: 32
- Процент отточных клиентов в первом сегменте: 5.545927209705372

Во-втором случае сегмент с лучшим показателями это:
Второй сегмент это клиенты с двумя продуктами:
- Размер второго сегмента:4981
- основное число клиентов пользуется двумя продуктами - 51.5 %, 
- с двумя продуктами больше клиентов мужского пола;
- с двумя продуктами также больше клиентов с кредитными картами чем без;
- активны и не склонны к оттоку;
- по баллам кредитного скоринга клиенты с двумя продуктами — от 800 до 880;
- для клиентов с двумя продуктами медианный баланс — 500000;
- для клиентов с двумя продуктами медианный оценочный доход — 100000;
- с двумя продуктами —  в среднем 3 балла собственности;
- процент оттока всего 19%
- больше всего клиентов с двумя продуктами проживает в Рыбинске.
К тому же судя про размеру это сегмент является ключевым.
Рекомендации:
- информировать о новых доступных банковских продуктах;
-для клиентов, получающих зарплату на карту другого банка - предложить льготные условия для перевода зарплаты в наш банк;
- предложить повышенный.

Но в то же время в ходе исследования мы обнаружили что клиенты с высокой оценкой дохода и балансом склонны к оттоку. Предлагается дополнительно ввести новые инвестиционные программы для клиентов с высоким доходом. А также не стоит перегружать клиентов количеством продуктов. Необходимо держать баланс на 2-3 продуктах  
