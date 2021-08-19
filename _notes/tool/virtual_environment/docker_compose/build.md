---
update: 2021-06-18
---

## Syntax

When `Dockerfile` and the context are in the same directory:

```yml
build: .
```

When setting custom dockerfile and context:

```yml
build:
  context: .
  dockerfile: dockerfiles/Dockerfile_app
```
