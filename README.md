# Дипломный проект

## Дипломная работа по модулю «Автоматизация тестирования»

Дипломная работа представляет собой автоматизацию тестирования веб-сервиса по покупке тура. После заполнения определенной формы сервис заносит информацию о покупке тура (одним из двух способов) в собственную БД и через API отсылает данные банковским сервисам на обработку.

### Начало работы

На компьютере, где запускается проект, должно быть установлено ПО: Git, IntelliJ IDEA, Docker Desktop.

1. Запустить настроенный Docker командой docker-compose up. 
2. В файле application.properties, который находится в корне проекта, необходимо внести следующие изменения:

    spring.credit-gate.url=http://localhost:9999/credit   
spring.payment-gate.url=http://localhost:9999/payment

3. Открыть IntelliJ IDEA
4. Скачать проект из репозитория Github локально с помощью команды
git clone https://github.com/Kotemako/diplom.git

### Запуск SUT, авто-тестов и генерация отчетов

1. В терминале IDEA запустить контейнеры:
   Запустить docker командой docker-compose up
2. В приложении IntelliJ IDEA в терминале прописать:

**Для MySQL:**

java -jar ./artifacts/aqa-shop.jar -- spring.datasource.url=jdbc:mysql://localhost:3306/app

**Для PostgreSQL:**

java -jar ./artifacts/aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app

3. В новой вкладке терминала в IDEA запустить тесты:

   **Для MySQL:**
./gradlew clean test -Durl=jdbc:mysql://localhost:3306/app

   **Для PostgreSQL:**
./gradlew clean test -Durl=jdbc:postgresql://localhost:5432/app


4. Для генерации отчета тестирования
.\gradlew allurereport Лог выполнения команды покажет, где расположен отчет: ..\build\reports\allure-report\allureReport\index.html


5. Для завершения работы allureServe выполнить команду Ctrl+C


6. Для остановки работы контейнера Docker выполнить команду
docker-compose down

### Документация проекта:
[1.Задание к диплому](https://github.com/Kotemako/Diplom/docs/Task.md)  
[2.План автоматизации](https://github.com/Kotemako/Diplom/docs/Plan.md)  
[3.Отчет по итогам тестирования](https://github.com/Kotemako/Diplom/docs/Report.md)