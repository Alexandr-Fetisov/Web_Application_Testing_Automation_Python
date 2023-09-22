# "Автоматизация тестирования веб-приложений на Python"
### Семинар - 1 Реализация тестирования API с использованием DDT:

*Задача_1:*

С использованием фреймворка pytest написать тест операции checkText
SOAP API https://speller.yandex.net/services/spellservice?WSDL
Тест должен использовать DDT и проверять наличие определенного
верного слова в списке предложенных исправлений к определенному неверному слову.
Слова должны быть заданы через фикстуры в conftest.py,
адрес wsdl должен быть вынесен в config.yaml.
Методы работы с SOAP должны быть вынесены в отдельную библиотеку.

*Задача_2:*

Написать тест с использованием pytest и requests, в котором:
- Адрес сайта, имя пользователя и пароль хранятся в config.yaml
- conftest.py содержит фикстуру авторизации по адресу https://test-stand.gb.ru/gateway/login с передачей параметров
“username" и "password" и возвращающей токен авторизации
- Тест с использованием DDT проверяет наличие поста с определенным заголовком в списке постов другого
пользователя, для этого выполняется get запрос по адресу
https://test-stand.gb.ru/api/posts c хедером, содержащим токен авторизации в параметре "X-Auth-Token". Для отображения
постов другого пользователя передается "owner": "notMe".

*Задача_3_ДЗ:*

Добавить в задание с REST API еще один тест, в котором создается новый пост,
а потом проверяется его наличие на сервере по полю “описание”.

Подсказка:

Создание поста выполняется запросом к https://test-stand.gb.ru/api/posts с передачей
параметров title, description, content.











