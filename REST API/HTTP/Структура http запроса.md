HTTP (Hypertext Transfer Protocol) запрос состоит из нескольких частей, включая метод запроса, заголовки и (в случае необходимости) тело запроса. Вот основные компоненты структуры HTTP запроса:

1. Метод запроса (Request Method):
    
    - Определяет тип операции, которую клиент хочет выполнить на сервере.
    - Некоторые распространенные методы запроса включают GET, POST, PUT, DELETE, HEAD, OPTIONS и другие.
    - Пример: GET, POST, PUT, DELETE
2. URI (Uniform Resource Identifier):
    
    - Идентификатор ресурса, на который клиент хочет выполнить операцию.
    - Может включать URL (Uniform Resource Locator) или URN (Uniform Resource Name).
    - Пример: /api/users/123, [https://example.com/products](https://example.com/products)
3. Протокол версии (Protocol Version):
    
    - Указывает на используемую версию протокола HTTP.
    - Пример: HTTP/1.1
4. Заголовки (Headers):
    
    - Поля, содержащие метаданные запроса, такие как информация о клиенте, тип контента, предпочитаемый язык и другие параметры.
    - Заголовки представляются в формате "Имя: Значение".
    - Пример: Content-Type: application/json, Accept-Language: en-US
5. Тело запроса (Request Body):
    
    - Необязательная часть, которая содержит данные, передаваемые в запросе.
    - Используется в запросах, таких как POST или PUT, где клиент отправляет данные на сервер.
    - Пример: {"name": "John", "age": 25}

Пример полного HTTP запроса может выглядеть следующим образом:

```
POST /api/users HTTP/1.1
Host: example.com
Content-Type: application/json
Authorization: Bearer <token>

{"name": "John", "age": 25}
```

Здесь мы видим метод POST, URI "/api/users", версию протокола HTTP/1.1, а также заголовки, такие как Host, Content-Type и Authorization. Также есть тело запроса в формате JSON, содержащее данные пользователя.

[[Идемпотентный запрос]]