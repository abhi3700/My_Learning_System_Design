# REST API

Also, covered websockets

## Overview

This is a REST API documentation for an application that allows users to create, read, update and delete (CRUD) data from a database.

---

**Routes vs Endpoints**

- A route is the URL (or path) that a client uses to communicate with the server.
- An endpoint is one end of a communication channel.

Suppose, for a TODO App:

| Route       | API endpoint | HTTP Method | CRUD Method | Description   |
| ----------- | ------------ | ----------- | ----------- | ------------- |
| /tasks      | /tasks       | GET         | READ        | Get all tasks |
| /tasks      | /tasks       | POST        | CREATE      | Create a task |
| /tasks/{id} | /tasks/{id}  | PUT         | UPDATE      | Update a task |
| /tasks/{id} | /tasks/{id}  | DELETE      | DELETE      | Delete a task |

Here, routes are 2, but endpoints are 4.

## Installation

VSCode - [Thunder Client](https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client)

## API data

- Free fake API for testing and prototyping: [Todo list](https://jsonplaceholder.typicode.com/todos)
- Create your API on this

## OpenAPI Specification

The Swagger UI is compatible with JSON, YAML as input/output parameters.

Example: https://petstore.swagger.io/

### Data Types

| type    | format   | Comments                        |
| ------- | -------- | ------------------------------- |
| integer | int32    | signed 32 bits                  |
| integer | int64    | signed 64 bits (a.k.a long)     |
| number  | float    |
| number  | double   |
| string  | password | A hint to UIs to obscure input. |

- primitive types: `integer`, `number` `string`, `boolean`.
- derived types: Object.

### Error Codes

| Code | Description           |
| ---- | --------------------- |
| 200  | OK                    |
| 201  | Created               |
| 204  | No Content            |
| 400  | Bad Request           |
| 401  | Unauthorized          |
| 403  | Forbidden             |
| 404  | Not Found             |
| 405  | Method Not Allowed    |
| 409  | Conflict              |
| 500  | Internal Server Error |

## REST API vs Websockets

Here are the key points from the [article](https://www.wallarm.com/what/websocket-vs-rest-api) titled "Websocket vs REST API. 💥 7 Significant Differences" from Wallarm, updated with emojis:

1. REST 🔄 and WebSocket 🌐 are two key technologies that developers deal with regularly. Understanding their differences and purposes is crucial for effective utilization 🎯.

2. REST is a collection of design principles or policies 📚 used extensively during web application/service development. It assists only HTTP protocol-based web application development. REST operations are stateless and standard, with every REST request created as per the HTTP verbs (GET, PUT, POST, and Delete) 📲.

3. The WebSocket protocol, contrary to REST, is stateful and helps two applications in seamless data transmission or information exchange 🔄. It's based on port & sockets and works only over a TCP connection. It supports bidirectional communication, meaning the same socket/port delivers and receives the data, establishing a continuous connection 🔗.

4. REST API exists to support stateless communication, where data is requested only when it's required by the web application. This is similar to the function of a vending machine 🏧, which provides goods only upon request.

5. WebSocket is used when an application demands ongoing or uninterrupted data delivery, such as in a chat application 💬. In such unbroken data delivery, using REST would be resource-extensive, whereas WebSocket simplifies the job 🎛️.

6. Key differences between WebSocket and REST include:

   - WebSocket is stateful and bidirectional, uses sockets and ports, and is used in the development of real-time applications ⏱️. It requires a unified TCP connection for client-server data exchange.
   - REST is stateless and unidirectional, and is useful when there is heavy request traffic for an application/solution 🚦. It requires a new TCP connection each time a request is made.

7. REST is suitable when data is available on an ad-hoc basis and diversity is required 🌈. WebSocket is ideal when the application should not miss a single entry in the delivery, such as applications demanding tick data analysis or where there is high load or request traffic 📈.

8. Regardless of the choice between REST and WebSocket, adopting stringent and robust API security 🔒 is a must as it leads to secure data transmission and exchange. It ensures that only secure APIs are used and data transmitted isn't in the reach of threat actors 🕵️‍♀️.

## Reference

- [OpenAPI Specification](https://swagger.io/specification/)
