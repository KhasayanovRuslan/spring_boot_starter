# spring_boot_starter
Задание: Создание Spring Boot Starter для логирования HTTP запросов

Описание:

Ваша задача - разработать Spring Boot Starter, который предоставит возможность логировать HTTP запросы в вашем приложении на базе Spring Boot.

Требования:

Функциональность:

Ваш Spring Boot Starter должен предоставлять возможность логировать все входящие и исходящие HTTP запросы и ответы вашего приложения.

Логирование должно включать в себя метод запроса, URL, заголовки запроса и ответа, код ответа, время обработки запроса и т.д.

Реализация:

Создайте проект Maven для вашего Spring Boot Starter.

Используйте Spring Boot для автоконфигурации вашего Starter.

Реализуйте механизм перехвата и логирования HTTP запросов с помощью фильтров или интерцепторов Spring, или Spring AOP.

Обеспечьте настройку уровня логирования и формата вывода логов.

Документация:

Напишите подробное описание вашего Spring Boot Starter, включая его функциональность и способы использования.

Обеспечьте хорошую документацию по API и конфигурации вашего Starter.

Тестирование:

Напишите unit-тесты для проверки корректности работы вашего Spring Boot Starter.

Покройте тестами основные сценарии использования и краевые случаи.

## Реализация
1. Реализована библиотека spring-boot-starter-logger, которая реализует логирование HTTP запросов.
2. Реализовано тестовое приложение book_application для проверки работы spring boot starter.

## Сборка и запуск
1. Склонируйте репозиторий:

<code>https://github.com/KhasayanovRuslan/spring_boot_starter.git</code>

2. Установите spring-boot-starter-logger в локальный maven репозиторий:

<code>cd spring_boot_starter/spring_boot_starter_logger</code>

<code>mvn clean install</code>

3. Проверка работы:
- Запустите book_application, предварительно настроив application.properties, по умолчанию логи сохраняются в папке logs.
- Подключите dependency к вашему проекту:
```
<dependency>
        <groupId>org.openschool</groupId>
        <artifactId>spring-boot-starter-logger</artifactId>
        <version>1.0-SNAPSHOT</version>
</dependency>
```

## Endpoints book_application:
- localhost:8080/books/one - POST запрос - добавляет одну книгу.
- localhost:8080/books/many - POST запрос - добавляет несколько книг.
- localhost:8080/books - GET запрос - получить все книги.
- localhost:8080/books/{name} - GET запрос - получить книгу по имени.
- localhost:8080/books/{name} - DELETE запрос - удалить книгу.
- localhost:8080/books/{name} - PUT запрос - обновить книгу.
- localhost:8080/books/category/{category} - GET запрос - возвращает все книги по категории.

         