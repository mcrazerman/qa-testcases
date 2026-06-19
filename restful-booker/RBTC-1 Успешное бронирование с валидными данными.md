**ID:** RBTC-1

**Заголовок:** Успешное бронирование с валидными данными 

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
  "checkin" : "2027-05-01", 
  "checkout" : "2027-05-15" }, 
"additionalneeds" : "Late checkout, WiFi"
}
```
**Шаги:**
1. Задать endpoint, метод, HTTP-заголовки запроса
2. Добавить тестовые данные в body запроса
3. Отправить запрос

**Ожидаемый результат:**
1. Статус код — `200 OK`
2. Формат ответа — json 
3. В ответе присутствует числовое поле bookingid
4. Вложенный объект booking полностью совпадает с отправленными тестовыми данными
5. Созданное бронирование успешно запрашивается через метод GET /booking/{bookingid}
