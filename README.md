# systems-analysis

## ES диаграмма
 - добавить скрин ES диаграммы
 - добавить ссылку на доску Miro


## Модель данных
 - добавить скрин модели данных
 - добавить ссылку на доску Miro


## Поддомены MCP

![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/f8db15dc-3859-497e-8d32-bd80ecc7d0af)


## Характеристики поддоменов

| Вид поддомена                                 | Конкурентное преимущество     | Сложность         | Изменчивость        | Варианты реализации     | Интерес проблемы       | Предполагаемый вид поддомена      |
|-----------------------------------------------|-------------------------------|-------------------|---------------------|-------------------------|------------------------|-----------------------------------|
| Работа с заказами                             | нет                           | высокая           | редкая              | купить готовое решение  | низкий                 | generic                           |
| Матчинг воркеров на заказы                    | да                            | высокая           | частая              | ???                     | высокий                | core                              |
| Хранение и сбор расходников                   | нет                           | низкая            | редкая              | ???                     | низкий                 | generic                           |
| Поиск и определение характеристик воркеров    | да                            | высокая           | частая              | ???                     | высокий                | core                              |
| Ставки                                        | нет                           | низкая            | редкая              | ???                     | низкий                 | supporting                        |


## MCP Core Domain Chart

![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/39c22515-55a8-4701-b251-3b54c1c9e233)


## Маппинг боундед-контекстов на поддомены

| Вид поддомена                                 | Предполагаемый вид поддомена      | Выделенный боундед-контекст                                                 |
|-----------------------------------------------|-----------------------------------|-----------------------------------------------------------------------------|
| Работа с заказами                             | generic                           | подписка на SaaS e-coTmmerce [elasticpath](https://www.elasticpath.com/)    |
| Матчинг воркеров на заказы                    | core                              | Система выбора воркера для заказа                                           |
| Хранение и сбор расходников                   | generic                           | Инвентаризация и склад                                                      |
| Поиск и определение характеристик воркеров    | core                              | ???                                                                         |
| Ставки                                        | supporting                        | Система ставок и определния победителей                                     |

![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/645b1216-f6f2-40f6-8b4a-d0041a9ee475)


## Сравнение разницы боундед-контекстов после из первого урока и после разбивки боунд-контекстов на поддомены

Элементы, получившиеся после первого урока:
![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/0a0f9714-afdb-4343-94a6-80a968bf8367)

В двух выделенных местах 5 боундед-контекстов из ES-модели, которые не сошлись с тем, что получилось после анализа поддоменов и боундед-контекстов.
![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/ef6e6491-6d07-4cbc-b8c6-0dc08d9b1552)

Проанализируем группу #2, состояющую из 2-х боундед-контекстов: поиска, определение характеристик воркера и матчинга. Изначально предполагалось, что
все процессы разбиваются на два контекста, при этом они связаны между собой, так как необходимы для определеня характеристик воркера и матчинга его на заказы.
Но после анализа поддоменов и боундед-контекстов оказалось, что поддомен "Поиск и определение характеристик воркеров" состоит из трех частей: 
Обработка заявок от воркеров-кандидатов и тестирование, определение характеристик, основанное на результатах тестирования, расчет и выплата зарплат и премий.
Получается, что, выбрав для поиска контекстов один только Event Storming, мы совершили ошибку.

Группировка сделанная изначально:                                                                                                | Группировка после анализа поддоменов и боундед-контекстов:
---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------
![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/f47ff83a-5c20-4780-afeb-6cb71714dd46)       | ![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/7c7cfcd1-999c-43a6-9107-ff49d0800c73)

Определяем связи между боундед-контекстами:
![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/858ae1c7-cc08-4305-ae30-a6925c5938cd)












