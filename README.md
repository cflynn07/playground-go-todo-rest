Playground Go TODO REST
=======================

Simple playground app to experiment with golang.

Goal is to build a TODO service with a RESTful HTTP API. Another goal is to unit test the code with
100% test coverage.

Notes
-----
- GoFMT is not 100% comprehensive. Lint tools for golang exist.
  - https://github.com/golang/lint
    - https://www.reddit.com/r/golang/comments/1xtcq9/lint_your_go_software_with_golint_engineered_web/
    - `golint` does not return non-zero if lint errors detected. `fgt` commonly used with `golint`
