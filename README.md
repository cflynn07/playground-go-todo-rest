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

- **HTTP Method + PATH**
  - `GET` /todos
- **Description**
  - Returns list of all TODOs
- **URL Params**
  - None
- **Data Params**
  - None
- **Success Response:**
- Code | Content
  -----|--------
  200  | `[{"id": 1, title: "Water Plants", "complete": true}, {"id": 2, title: "Walk Dog", "complete": false}]`

- **Error Response:**
  None

---

- **HTTP Method + PATH**
  - `GET` /todos
- **Description**
  - Returns list of all TODOs
- **URL Params**
  - None
- **Data Params**
  - None
- **Success Response:**
- Code | Content
  -----|--------
  200  | `[{"id": 1, title: "Water Plants", "complete": true}, {"id": 2, title: "Walk Dog", "complete": false}]`

- **Error Response:**
  None
