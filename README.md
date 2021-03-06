Playground Go TODO REST
=======================

Simple playground app to experiment with golang.

Goal is to build a TODO service with a RESTful HTTP API. Another goal is to unit test the code with
100% test coverage.

## Notes

- GoFMT is not 100% comprehensive. Lint tools for golang exist.
  - https://github.com/golang/lint
    - https://www.reddit.com/r/golang/comments/1xtcq9/lint_your_go_software_with_golint_engineered_web/
    - `golint` does not return non-zero if lint errors detected. `fgt` commonly used with `golint`
- `glide` bills itself the `npm` of go.
  - https://github.com/Masterminds/glide
  - https://blog.gopheracademy.com/advent-2015/vendor-folder/
  - `npm init` ~= `glide create`
  - `npm install foo --save` ~= `glide get github.com/foo_org/foo`
  - `/vendor` folder notes:
    - https://blog.gopheracademy.com/advent-2015/vendor-folder/
    - "Advice on how to use the vendor folder is varied. Some will shutter at
      the thought of including dependencies in the project repository. Others
      hold it is unthinkable to not include the dependencies in the project
      repository. Some will just want to include a manifest or lock file and
      fetch the dependencies before building."

## API Documentation

- All HTTP request bodies should be JSON strings

- **HTTP Method + PATH**
  - `GET` /todos
- **Description**
  - Return a list of all todos.
- **URL Params**
  - None
- **Body Params**
  - None
- **Success Response:**

Code | Example Content
-----|----------------
200  | `[{"id": 1, title: "Water Plants", "complete": true}, {"id": 2, title: "Walk Dog", "complete": false}]`

- **Error Responses:**
  None

---

- **HTTP Method + PATH**
  - `PUT` /todos/:id
- **Description**
  - Modify the value of the `complete` property of a todo.
- **URL Params**
  - None
- **Body Params**

Key      | Type    | Required
---------|---------|---------
complete | boolean | true

- **Success Responses:**

Code | Example Content
-----|----------------
200  | `{"id": 2, title: "Walk Dog", "complete": true}`

- **Error Responses:**

Code | Example Content
-----|----------------
400  | `{"error": "Bad Request"}`
404  | `{"error": "Not Found"}`

---

- **HTTP Method + PATH**
  - `POST` /todos
- **Description**
  - Create a new todo.
- **URL Params**
  - None
- **Body Params**

Key   | Type    | Required
------|---------|---------
title | string  | true


- **Success Responses:**

Code | Example Content
-----|----------------
201  | `{"id": 2, title: "Walk Dog", "complete": false}`

- **Error Responses:**

Code | Example Content
-----|----------------
400  | `{"error": "Bad Request"}`
