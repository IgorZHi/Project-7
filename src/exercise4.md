## Тестирование API с Postman

https://blue-crescent-476339.postman.co/workspace/My-Workspace~6587acb9-df1f-43e5-85a2-6ba02a731210

### Отчёт запросов и ответов Fake REST Api.


#### Activities :

***GET ​/api​/v1​/Activities***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат** - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 120a2e4c-c0c2-471e-b19f-6f72dbd7c92b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса** Отсутствует


**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 20:43:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"title":"Activity 1","dueDate":"2023-06-14T21:43:43.9031735+00:00","completed":false},{"id":2,"title":"Activity 2","dueDate":"2023-06-14T22:43:43.903176+00:00","completed":true},{"id":3,"title":"Activity 3","dueDate":"2023-06-14T23:43:43.9031764+00:00","completed":false},


***POST ​/api​/v1​/Activities***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9edb8174-3727-4376-998e-138fe29f6fb2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-13T11:57:51.020Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 20:53:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","dueDate":"2023-06-13T11:57:51.02Z","completed":true}

***GET ​/api​/v1​/Activities​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: cb6795df-b0b0-4ad1-9d01-53202f1b790c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 21:02:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"title":"Activity 1","dueDate":"2023-06-14T22:02:17.9537052+00:00","completed":false}


***GET ​/api​/v1​/Activities​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 08da7a6f-5615-4860-b30b-c5f8d65479ff
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 21:06:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-572c0cfd8407c240ad1d28a9f91de03a-bb2eb1d2da09484e-00"}


***PUT ​/api​/v1​/Activities​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a8bbe2d8-c87c-4c24-9dc0-aba3374a14ea
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-13T13:17:50.679Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 21:09:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","dueDate":"2023-06-13T13:17:50.679Z","completed":true}


***PUT ​/api​/v1​/Activities​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{body_no}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: cbb9f358-b974-4f80-b798-8dd9f52cfb5b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Wed, 14 Jun 2023 21:48:06 GMT
Server: Kestrel
Allow: GET, POST

**Тело ответа**

0


***PUT ​/api​/v1​/Activities​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{body_word}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 510953e3-7b69-40ff-8f4c-e4b1aebfcec3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": put,
  "title": "string",
  "dueDate": "2023-06-13T14:41:11.361Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Wed, 14 Jun 2023 21:53:58 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-f6ff49391c14db4f9e4ca1921e08d8e7-aa1b6f7a40f47a43-00","errors":{"id":["The value 'post put' is not valid."],"$.id":["'p' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."]}}



***DELETE ​/api​/v1​/Activities​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: bfd7b200-3753-48f0-80d3-afa15734c0b5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Wed, 14 Jun 2023 21:56:56 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**

0


***DELETE ​/api​/v1​/Activities​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{12_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 491e1636-4e3e-4ee4-9eaf-031ca8b3eff3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Wed, 14 Jun 2023 21:59:51 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

0


***GET ​/api​/v1​/Activities​/{id}*** (BAG)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{bag_id}}

**Ожидаемый результат**  - получить запрос c кодом 200 (а получаем 404)

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e95d9c6b-6a1d-4d85-881d-615e7662ac51
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 22:03:35 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-fe4e97ed029508408f25c849b697e572-e25333a49628bb45-00"}



***POST ​/api​/v1​/Activities*** ( BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат**  - получить запрос c 400 в свагере 200 получаем. Здесь 405

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: b81645af-f92c-4dcb-9241-5a0c693b9b05
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "title": "string",
  "dueDate": "2023-06-14T14:12:40.517Z",
  "completed": true
}

**Заголовки ответа**

Content-Length: 0
Date: Wed, 14 Jun 2023 22:08:00 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0


***PUT ​/api​/v1​/Activities​/{id}*** (BAG)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат**  - получить запрос 400 ,(получаем 200)

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 272866b8-fd40-41fd-bbb0-9d33ec95fc4b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-14T14:17:34.092Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 22:13:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","dueDate":"2023-06-14T14:17:34.092Z","completed":true}


***PUT ​/api​/v1​/Activities​/{id}*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 ( получаем 200)

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 64542bb4-2a16-4412-af14-d06e1558cf6f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "title": "string",
  "dueDate": "2023-06-14T14:17:34.092Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 22:18:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"title":"string","dueDate":"2023-06-14T14:17:34.092Z","completed":true}



### Authors

***GET ​/api​/v1​/Authors***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 526a5585-a79b-47ff-84f5-1497e2e95dd9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Wed, 14 Jun 2023 22:24:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"},{"id":2,"idBook":1,"firstName":"First Name 2","lastName":"Last Name 2"},{"id":3,"idBook":1,"firstName":"First Name 3","lastName":"Last Name 3"},{"id":4,"idBook":1,"firstName":"First Name 4","lastName":"Last Name 4"},


***POST ​/api​/v1​/Authors***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d6ec2bde-a383-4dfa-9301-5b57c2cd1703
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 06:51:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"firstName":"string","lastName":"string"}


***POST ​/api​/v1​/Authors***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_no}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 34ff9233-7406-4f42-a78c-b3a342bd9bf3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 06:54:33 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.13","title":"Unsupported Media Type","status":415,"traceId":"00-9b303e437ec7b94887585c07a0456df9-c59a4841fc751c45-00"}


***POST ​/api​/v1​/Authors***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_word}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c99ab6f2-741a-4a81-8d62-072358b61fda
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": post,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 06:57:44 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0


***GET ​/api​/v1​/Authors​/authors​/books​/{idBook}***



**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7384f004-7532-4c12-9c06-fe47fec745bc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:01:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[{"id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"},{"id":2,"idBook":1,"firstName":"First Name 2","lastName":"Last Name 2"}]



***GET ​/api​/v1​/Authors​/authors​/books​/{idBook}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{12_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a6a47989-48db-45a8-b6b7-5c9bd2819131
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0
**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 07:04:01 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-d3106340761be74c9725fb8056a464a1-b3e7026c672a9e48-00","errors":{"idBook":["The value '111111111111' is not valid."]}}



***GET ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0c0ee045-6d77-4b62-ad86-9e74193c75d5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:06:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"}


***GET ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{12_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 994959c2-113d-4682-8b10-1433b9fbf7db
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 07:08:43 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-9b4048c7a40d42419e59b15472897203-4bb9fe81a5dd0e42-00","errors":{"id":["The value '111111111111' is not valid."]}}



***PUT ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 333f4173-5cfc-4b6b-9e75-38c8e6cd89ad
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:11:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"firstName":"string","lastName":"string"}



***PUT ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{12_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 36da4a6b-c225-4325-b6e9-2c678937f6a9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 07:16:24 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-d3ca8c3792458d45b2068b01a0155624-0f415575d1ec9c4f-00","errors":{"id":["The value '111111111111' is not valid."]}}



***PUT ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_no}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 74ca5a3f-8f48-40d8-8167-d8e4e05d7723
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 07:18:43 GMT
Server: Kestrel
Allow: GET, POST

**Тело ответа**
0


***PUT ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_word}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 49eff58c-6524-4886-9b3f-105e8f977005
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": put,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 07:20:22 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-9d94d80bd08bce4690d5fbaf96091a8d-2f795622c5dd764a-00","errors":{"id":["The value 'post put' is not valid."],"$.id":"'p' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."}}


***DELETE ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 227f4429-936b-4c2a-8ef9-57a5fb3bf333
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 07:22:33 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**
0



***DELETE ​/api​/v1​/Authors​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{12_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 88d137a3-f463-4553-b196-6b3d9faa35c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 07:24:41 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**
0



***POST ​/api​/v1​/Authors*** (BAG)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{minus_id}}

**Ожидаемый результат**  - получить запрос с ошибкой 400 (-1 в тело запроса вводим) в свагере код 200 показывает . здесь 415

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ce96917f-f325-4174-a7de-3ac57a788c2c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 07:26:59 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**
0



***PUT ​/api​/v1​/Authors​/{id}*** (BAG)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 а получаем с 200 вводя -1

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 005f361f-9039-41ba-b96e-bb6753d574dc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:31:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"firstName":"string","lastName":"string"}




***PUT ​/api​/v1​/Authors​/{id}*** (BAG)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 а получаем - 200 вводя -1 в тело запроса.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b9940c6b-c58a-490e-b96a-85ed95abcd4f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:41:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"idBook":0,"firstName":"string","lastName":"string"}


### Books


***GET ​/api​/v1​/Books***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2730575a-4215-432a-891e-184262cd132b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:46:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

"id":1,"title":"Book 1","description":"Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n","pageCount":100




***POST ​/api​/v1​/Books***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cfb8aca3-2c2a-4f3c-980e-1a3bd716b0a6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T16:30:48.937Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:49:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-13T16:30:48.937Z"}



***GET ​/api​/v1​/Books​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f5907055-a788-4c11-9aa6-3463c7fc8d78
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 07:51:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


**Тело ответа**

"id":1,"title":"Book 1","description":"Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n","pageCount":100,"excerpt"


***GET ​/api​/v1​/Books​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3dcb51fe-c6aa-47dc-ba0b-69af41fcabbd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 08:10:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-83533691e90c354a9c0164386a73a937-ff45cc712d32f64f-00"}


***PUT ​/api​/v1​/Books​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a3ea9bd7-bdef-4b34-8e90-2e68ec50d9e4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T16:38:42.901Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 08:12:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-13T16:38:42.901Z"}


***PUT ​/api​/v1​/Books​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{body_no}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 71f403ba-8008-4bb4-bfed-5a3f66c35a27
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T16:38:42.901Z"
}

**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 08:17:35 GMT
Server: Kestrel
Allow: GET, POST

**Тело ответа**
0



***PUT ​/api​/v1​/Books​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{body_word}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a957b280-ff04-4404-bbbf-45eac11219bb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
 
{
  "id": ,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-13T16:38:42.901Z"
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 08:20:39 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-08dfd498d1d9aa4a88dee15e3e697ff8-7d1dea78fb93fd41-00","errors":{"id":["The value 'post put' is not valid."],"$.id":',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."}}


***DELETE ​/api​/v1​/Books​/{id}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 260c9632-d77d-4e00-913f-c43e5149d536
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 08:22:50 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**
0



***POST ​/api​/v1​/Books*** (БАГ)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 а получаем с кодом 200 в свагере , здесь 405

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 156ec65f-eb1b-4d24-aa4d-e3a47cf71ed0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-14T14:30:03.334Z"
}

**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 08:24:34 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**
0



***PUT ​/api​/v1​/Books​/{id}*** (БАГ)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат**  - получить запрос 400 а получаем 200 вводя в ID -1

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 140ddaa5-3b99-49ff-9fb9-96cca7403a19
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-14T14:31:43.538Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 08:29:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-14T14:31:43.538Z"}



***PUT ​/api​/v1​/Books​/{id}*** (БАГ)


**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 а получаем код 200 вводя в тело запроса -1

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 57ec4d25-f101-4a57-9992-6612623b5f04
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id":-1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-14T14:31:43.538Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 08:32:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-14T14:31:43.538Z"}


### CoverPhotos


***GET ​/api​/v1​/CoverPhotos***


**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8571ba20-5f81-4157-b20e-e3672eced4db
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:05:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"idBook":1,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"},{"id":2,"idBook":2,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"},{"id":3,"idBook":3,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"},


***POST ​/api​/v1​/CoverPhotos***


**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 4b89bc22-c9e3-4145-9ddc-5eecaf9c080b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:10:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"url":"string"}

***GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}***


**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b069eefa-87d7-4336-a833-344abdf6a16c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:13:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[{"id":1,"idBook":1,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"}]


***GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{minus_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9ea1faf8-ce28-46d4-a74c-f1044d1a62bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:15:46 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[]

***GET ​/api​/v1​/CoverPhotos​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 5719ebdf-50af-42b5-a975-9b203555d357
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:17:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


**Тело ответа**

[{"id":1,"idBook":1,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"}]


***GET ​/api​/v1​/CoverPhotos​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{minus_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 53abfd85-59a0-467e-ba86-2aa2de8a6174
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:19:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[]

***PUT ​/api​/v1​/CoverPhotos​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{body_0}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b9c9319b-af1f-4475-8986-e1023586a790
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:21:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"url":"string"}

PUT
​/api​/v1​/CoverPhotos​/{id}

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e3b530ba-6921-4469-a21c-4b1054103f5d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 1,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:24:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"idBook":0,"url":"string"}

***DELETE ​/api​/v1​/CoverPhotos​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 581d2436-9c2c-4d52-939a-502aa8c0f035
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 11:26:21 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**
0

***POST ​/api​/v1​/CoverPhotos***  (БАГ)


**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 . а получаем с кодом 200 в свагере и здесь с кодом 404

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e6950cc8-86a7-49e9-ba74-e93529ccd58c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 11:28:34 GMT
Server: Kestrel

**Тело ответа**

0

***PUT ​/api​/v1​/CoverPhotos​/{id}*** (БАГ)


**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 . а получаем с кодом 200.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2cccb358-f9db-43de-a25e-05f20dd2bda4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:33:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"url":"string"}



***PUT ​/api​/v1​/CoverPhotos​/{id}*** (БАГ)


**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 . а получаем с кодом 200.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: de848d6d-26a5-47bf-a375-f09cbc9695a5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:36:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"idBook":0,"url":"string"}


## Users


***GET ​/api​/v1​/Users***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c76aaeb2-d78a-453e-8aa6-e58666565e99
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:10:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"userName":"User 1","password":"Password1"},{"id":2,"userName":"User 2","password":"Password2"},



***POST ​/api​/v1​/Users***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users{{activity_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d30f8231-1740-48a0-93d2-40d00fa2cac0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:15:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


**Тело ответа**

{"id":0,"userName":"string","password":"string"}




***GET ​/api​/v1​/Users​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 975c2501-4aa0-4854-9c2f-601f7ed2faf3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:17:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"userName":"User 1","password":"Password1"}




***GET ​/api​/v1​/Users​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: bab9b1c0-0306-4280-b857-32a66805b368
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:20:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-27008e01c15282448a596170961b42de-7b2bed9850825c43-00"}




***PUT ​/api​/v1​/Users​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9b0b4f01-3916-4ff5-b308-5d3fff1dedb2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:21:58 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"userName":"string","password":"string"}




***DELETE ​/api​/v1​/Users​/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{one_id}}

**Ожидаемый результат**  - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6f6e29aa-f58e-4ef9-b874-3456a646e1e0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 12:24:19 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**
0



***GET ​/api​/v1​/Users​/{id}*** (БАГ )

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{bag_id}}

**Ожидаемый результат**  - получить запрос с кодом 200 , а получаем 404 

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7c035789-78c1-42bc-a32f-7aa95b19cc69
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0
**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:27:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-e138e51e5f53794ebb4006998473c7bf-ffb77fbe02e40e41-00"}


***POST ​/api​/v1​/Users***   (Баг)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  - получить запрос 400 а получаем 200 в свагере и 405 здесь

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0c3781d6-2249-47f1-88b6-52b1d16d1c17
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Thu, 15 Jun 2023 12:30:57 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**
0



***PUT ​/api​/v1​/Users​/{id}***   (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 , а получаем с кодом 200 вводя -1 в ID запроса.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 31b3893f-89d6-4a1f-8c66-59ce09f4b386
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:34:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"userName":"string","password":"string"}


***PUT ​/api​/v1​/Users​/{id}***    (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 , получаем с кодом 200 вводя -1 в тело запроса.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2a761e0e-2bb5-4b27-8ecf-9cc15f6eb28e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:37:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"userName":"string","password":"string"}
