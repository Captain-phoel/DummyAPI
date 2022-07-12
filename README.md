# DummyAPI
Представлено описание тестирования проекта DummyAPI.

## Оглавление

## Описание проекта
https://dummyapi.io/ - сервис для тестирования API. В качестве тестирования был взят объект **POST**.

### POST
____
#### GET /post (Get List)
Возвращает список публикаций отсортированных по дате создания.
- доступен query params для вывода определённой страницы

**Response Body**

**List**
```js
{
  data: Array(Model)
  total: number(total items in DB)
  page: number(current page)
  limit: number(number of items on page)
}
```

#### GET//user/:id/post (Get List By User)
Возвращает список публикаций конкретного юзера.
- доступен query params для вывода определённой страницы
- 
**Response Body**

**List**
```js
{
  data: Array(Model)
  total: number(total items in DB)
  page: number(current page)
  limit: number(number of items on page)
}
```

____
## Майнд-карта
Данная МК представляет собой набор тестов для тестирования объекта **POST**. 
[Ссылка на МК](https://mind42.com/mindmap/032dcfd4-f2c5-49a1-a2c9-22973e9d4c36).

## Тест-кейсы
Также были оформлены тест-кейсы в соответствии с майнд-картой.
Тест-кейсы можно посмотреть тут.

## Баг-репорты

## Коллекции Postman
