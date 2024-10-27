# Bankovsky-
left to right direction
actor "Читатель" as Reader
actor "Библиотекарь" as Librarian

rectangle "Система управления библиотекой" {
usecase "Регистрация читателя" as Registration
usecase "Поиск книги" as Search
usecase "Выдача книги" as Issue
usecase "Возврат книги" as Return

Reader --> Return: Вернуть книгу в библиотеку

Librarian --> Issue: Зарегистрировать выдачу книги
Librarian --> Return: Принять книгу при возврате
Reader --> Registration: Выполнить регистрацию
Reader --> Search: Найти нужную книгу
Reader --> Issue: Получить книгу на руки
