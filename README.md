# User Account Service

 Стек технологий
- Java 11
- Spring Boot
- PostgreSQL
- Spring Data JPA
- Redis
- JWT (JJWT)
- Swagger (springdoc-openapi)
- Maven
- Testcontainers

 Запуск проекта

1. в PostgreSQL создайте БД:

CREATE DATABASE testdb;


2. Изменить настройки доступа в `application.yaml`:
  yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/testdb
    username: postgres
    password: postgres


3. Запустить Redis локально (по умолчанию порт 6379).

4. Соберите и запустите проект:

mvn clean install
mvn spring-boot:run

либо же опционально через плашку М

5. Swagger по адресу:http://localhost:8080/swagger-ui.html


- JWT авторизация по email+password и phone+password.
- Расширение баланса каждые 30 секунд (до 207% от первоначального значения).
- Потокобезопасный перевод средств между пользователями с валидацией.
- Кэширование в DAO и API слоях (Redis).
- Поиск пользователей с пагинацией и фильтрацией.
- Unit-тесты + интеграционные тесты с Testcontainers.

Тестирование
mvn test

