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

#### GET /user/:id/post (Get List By User)
Возвращает список публикаций конкретного юзера.
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

#### GET /tag/:id/post (Get List By Tag)
Возвращает список публикаций с указанным тэгом.
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

#### GET /post/:id (Get Post by id)
Вовзращает публикацию по указанному айди. 

**Response Body**

**Full**
```js
{
  id: string(autogenerated)
  text: string(length: 6-1000)
  image: string(url)
  likes: number(init value: 0)
  link: string(url, length: 6-200)
  tags: array(string)
  publishDate: string(autogenerated)
  owner: object(User Preview)
}
```

#### POST /post/create (Create Post)
Создаёт новую публикацию и возвращает информацию по ней.

**Request Body**

Обязательные поля - "owner" и "post".

```js
{
  text: string(length: 6-50, preview only)
  image: string(url)
  likes: number(init value: 0)
  tags: array(string)
  owner: string(User id)
}
```

**Response Body**

**Full**
```js
{
  id: string(autogenerated)
  text: string(length: 6-1000)
  image: string(url)
  likes: number(init value: 0)
  link: string(url, length: 6-200)
  tags: array(string)
  publishDate: string(autogenerated)
  owner: object(User Preview)
}
```

### PUT /post/:id (Update Post)
Обновляет информацию о публикации по айди, возвращает обновлённую информацию о публикации.

**Request Body**

Запрещено обновлять поле "owner".

```js
{
  text: string(length: 6-50, preview only)
  image: string(url)
  likes: number(init value: 0)
  tags: array(string)
}
```

**Response Body**

**Full**
```js
{
  id: string(autogenerated)
  text: string(length: 6-1000)
  image: string(url)
  likes: number(init value: 0)
  link: string(url, length: 6-200)
  tags: array(string)
  publishDate: string(autogenerated)
  owner: object(User Preview)
}
```

#### Delete /post/:id (Delete Post)
Удаляет публикацию по указанному айди, возвращает айди удалённой публикации.

**Response Body**

```js
{
  id: string
}
```
____
## Майнд-карта
[.Данная МК](https://mind42.com/mindmap/032dcfd4-f2c5-49a1-a2c9-22973e9d4c36) представляет собой набор тестов для тестирования объекта **POST**. 


## Коллекции Postman
Коллекции и окружение можно посмотреть в прикреплённых файлах.
Post.postman_collection - коллекция запросов автотестами к объекту Post.
DummyAPI GetList&CreatePost tests.postman_collection - коллекция тестовых запросов, составленных на основе Майнд-карты к роутам GetList & CreatePost.
