# REST API

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

## Reference

- [OpenAPI Specification](https://swagger.io/specification/)
