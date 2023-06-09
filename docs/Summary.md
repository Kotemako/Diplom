## Отчет по итогам автоматизации
### Выполнено:
* Проведено автоматизированное UI-тестирование всех запланированных позитивных и негативных сценариев для обоих вариантов взаимодействия с сервисом: "Оплата по карте" и "Кредит по карте"
* Проведено тестирование API сервиса для оплаты покупки тура с использованием Postman
* Проиведена корректная настройка работы БД MySQL и PostgeSQL с SUT
* Составлен отчет по итогам автоматизации
* Составлены 10 issues по найденным дефектам
___

### Сработавшие риски
* Из-за отсутствия документации по проекту было трудно догадаться, какой именно будет ответ при том или ином запросе;
* Сложность в установке сразу двух БД
* Неработоспособность подготовленного симулятора банковских сервисов - по причине неработоспособности Docker'a не было возможности запустить сервис aqa-shop.jar
___

### Общий итог по времени
1. Настройка SUT: запланировано 5 часов, фактически - 15 часов.
2. Разработка тест-плана: запланировано 5 часов, фактически - 25 часов.
3. Написание авто-тестов и их прогон: запланировано 50 часов, фактически - 40 часов.
4. Написание баг-репортов: запланировано 10 часов, фактически - 15 часов.
5. Написание отчета по результатам автоматизации: запланировано 10 часов, фактически 2 часа.

#### Итого: запланировано 80 часов, фактически 97 часов