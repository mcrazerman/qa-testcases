**ID:** RBTC-4

**Заголовок:** Ошибка бронирования при указании некорректных дат

**Приоритет:** High

**Предусловия:**
1. Endpoint - [https://restful-booker.herokuapp.com/booking](https://restful-booker.herokuapp.com/booking) 
2. Метод — `POST` 
3. HTTP-заголовки: `Content-Type: application/json`; `Accept:application/json`

**Тестовые данные:**
```json
{ 
"firstname" : "Bulat", 
"lastname" : "QA-Engineer", 
"totalprice" : 1500, 
"depositpaid" : true, 
"bookingdates" : { 
  "checkin" : "2027-06-01", 
  "checkout" : "2027-05-15" }, 
"additionalneeds" : "Late checkout, WiFi"
}
```

**Шаги:**
1. Задать endpoint, метод, HTTP-заголовки запроса
2. Добавить тестовые данные в body запроса
3. Отправить запрос

**Ожидаемый результат:**
1. Статус код — `400 Bad Request`
2. В ответе содержится сообщение об ошибке `checkin date must be earlier than checkout date`
3. Новое бронирование не создаётся
