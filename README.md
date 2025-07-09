# Тестирование API сервиса JSONPlaceholder с помощью Postman

Этот репозиторий является примером моей работы как QA-инженера и демонстрирует навыки автоматизированного тестирования API с использованием Postman.

##  Цель проекта

Создать коллекцию запросов в Postman для тестирования основных эндпоинтов (`/posts`) публичного API [JSONPlaceholder](https://jsonplaceholder.typicode.com/). Продемонстрировать умение работать с различными типами HTTP-запросов (GET, POST, PUT, DELETE), использовать переменные окружения и писать автотесты на JavaScript.

##  Использованные технологии

*   **Postman:** для создания и отправки запросов.
*   **JavaScript:** для написания скриптов автотестов в Postman.
*   **Chai Assertion Library (встроен в Postman):** для проверок в тестах.

##  Как использовать

1.  **Клонируйте репозиторий или скачайте файлы:**
    *   `JSONPlaceholder.postman_collection.json` - основная коллекция запросов.
    *   `JSONPlaceholder.postman_environment.json` - переменные окружения (содержит `baseUrl`).

2.  **Импортируйте файлы в Postman:**
    *   Откройте Postman и нажмите кнопку **"Import"**.
    *   Перетащите или выберите оба скачанных файла.
    *   Postman автоматически импортирует коллекцию и окружение.

3.  **Выберите окружение:**
    *   В правом верхнем углу Postman убедитесь, что выбрано окружение `JSONPlaceholder Env`.

4.  **Запускайте запросы:**
    *   Вы можете запускать запросы по одному или запустить всю коллекцию сразу через **"Collection Runner"**.

##  Описание тестов и запросов

Коллекция включает следующие запросы с автотестами:

### `[GET] All Posts`
*   Получает список всех постов.
*   **Тесты:**
    *   `Status code is 200`
    *   `Response body is an array`
    *   `Response array is not empty`

### `[GET] Single Post`
*   Получает один пост по `id=1`.
*   **Тесты:**
    *   `Status code is 200`
    *   `Response body has 'userId' property`
    *   `Post ID is 1`

### `[POST] Create Post`
*   Создает новый пост.
*   **Тесты:**
    *   `Status code is 201`
    *   `Title is correct`

### `[PUT] Update Post`
*   Обновляет пост с `id=1`.
*   **Тесты:**
    *   `Status code is 200`
    *   `Title was updated`

### `[DELETE] Delete Post`
*   Удаляет пост с `id=1`.
*   **Тесты:**
    *   `Status code is 200`
    *   `Response body is empty`
