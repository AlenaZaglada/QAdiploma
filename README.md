# Дипломный проект по курсу «Тестировщик ПО»

# Запуск приложения
Перед запуском необходимо выполнить следующие предусловия. Если у вас уже есть необходимое ПО, то понадобится только п.1 и запуск Docker.

**Предусловия**

Необходимо склонировать репозиторий или скачать архив по ссылке. Или воспользоваться VCS Git, встроенной в IntelliJ IDEA.
Установать и запустить Docker Desktop. Это можно сделать здесь в зависимости от операционной системы. Дополнительные инструкции можно найти по ссылке
Открыть проект в IntelliJ IDEA

**Запуск**
Запустить необходимые базы данных (MySQL и PostgreSQL), а также NodeJS. Параметры для запуска хранятся в файле docker-compose.yml. Для запуска необходимо ввести в терминале команду:

docker-compose up

В новой вкладке терминала ввести следующую команду в зависимости от базы данных

- java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar 
- java "-Dspring.datasource-postgresql.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar - для PostgreSQL

Приложение должно запуститься
![image](https://github.com/AlenaZaglada/QAdiploma/assets/121796172/bfe3a9a1-928e-4070-80e8-c2662b533fa1)
работать по адресу http://localhost:8080/

# Запуск тестов
В новой вкладке терминала ввести команду: 

#В новой вкладке терминала ввести команду в зависимости от запущенной БД в п.2 Запуска:
- ./gradlew clean test "-Ddb.url=jdbc:mysql://localhost:3306/app" - для MySQL
- ./gradlew clean test "-Ddb.url=jdbc:postgresql://localhost:5432/app" - для PostgreSQL

./gradlew clean test

# Формирование отчета AllureReport по результатам тестирования
В новой вкладке терминала или нажав двойной Ctrl ввести команду:

./gradlew allureReport


