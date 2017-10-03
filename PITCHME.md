---

### Основы HTTP

---

### Базовые принципы HTTP

HTTP - протокол прикладного уровня передачи данных согласно модели OSI. Основой HTTP является технология «клиент-сервер», то есть предполагается существование:

* Потребителей (клиентов), которые инициируют соединение и посылают запрос;
* Поставщиков (серверов), которые ожидают соединения для получения запроса, производят необходимые действия и возвращают обратно сообщение с результатом.

+++

Текстовый протокол без сессий и состояний

```
user (request) -> server
user <- (response) server
```

+++

### Пример запроса HTTP

```
telnet google.com 80

GET / HTTP/1.1      <-- request line
host: google.com    <-- обязательный атрибут виртуальный хост
user-agent: mozilla
connection: close | keep-alive

```

+++

### Тело запроса

```
telnet google.com 80

POST / HTTP/1.1
host: google.com
content-length: 28
connection: close
content-type: text/plain | application/octet-stream
```

+++

### Отправка форм

```
telnet google.com 80

POST / HTTP/1.1
host: google.com
content-length: 28
content-type: application/x-www-form-urlencoded
```

```
login=log in1&password=pass=20

login=log%20in1&password=pass%3D20
```