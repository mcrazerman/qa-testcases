**ID:** RBTC-2

**Заголовок:** Ошибка бронирования при передаче пустого запроса

**Приоритет:** Medium

**Предусловия:**
1. Endpoint - [https://restful-booker.herokuapp.com/booking](https://restful-booker.herokuapp.com/booking) 
2. Метод — `POST` 
3. HTTP-заголовки: `Content-Type: application/json`; `Accept:application/json`

**Тестовые данные:**
```json
{}
```

**Шаги:**
1. Задать endpoint, метод, HTTP-заголовки запроса
2. В качестве тела запроса указать пустой объект `{}`
3. Отправить запрос

**Ожидаемый результат:**
1. Статус код — `400 Bad Request`
2. В ответе содержится сообщение об ошибке `Invalid Input`
3. Новое бронирование не создаётся
