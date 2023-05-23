# systems-analysis

## Поддомены MCP

![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/601ffdb6-3b27-4bbd-aa06-8e0010efeedd)


## Характеристики поддоменов

| Вид поддомена                                 | Конкурентное преимущество     | Сложность         | Изменчивость        | Варианты реализации     | Интерес проблемы       | Предполагаемый вид поддомена      |
|-----------------------------------------------|-------------------------------|-------------------|---------------------|-------------------------|------------------------|-----------------------------------|
| Работа с заказами                             | нет                           | высокая           | редкая              | купить готовое решение  | низкий                 | generic                           |
| Матчинг воркеров на заказы                    | да                            | высокая           | частая              | ???                     | высокий                | core                              |
| Хранение и сбор расходников                   | нет                           | низкая            | редкая              | ???                     | низкий                 | generic                           |
| Поиск и определение характеристик воркеров    | да                            | высокая           | частая              | ???                     | высокий                | core                              |
| Ставки                                        | нет                           | низкая            | редкая              | ???                     | низкий                 | supporting                        |


## MCP Core Domain Chart

![изображение](https://github.com/mechanicalmachine/systems-analysis/assets/30704273/1170dcdd-233d-41a0-8d81-07d07b9e936d)


## Маппинг боундед-контекстов на поддомены

| Вид поддомена                                 | Предполагаемый вид поддомена      | Выделенный боундед-контекст                                                 |
|-----------------------------------------------|-----------------------------------|-----------------------------------------------------------------------------|
| Работа с заказами                             | generic                           | подписка на SaaS e-coTmmerce [elasticpath](https://www.elasticpath.com/)    |
| Матчинг воркеров на заказы                    | core                              | Система выбора воркера для заказа                                           |
| Хранение и сбор расходников                   | generic                           | Инвентаризация и склад                                                      |
| Поиск и определение характеристик воркеров    | core                              | ???                                                                         |
| Ставки                                        | supporting                        | Система ставок и определния победителей                                     |
