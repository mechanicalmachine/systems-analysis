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

