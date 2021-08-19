---
doc: https://docs.docker.com/compose/compose-file/compose-file-v3/#logging
update: 2021-06-15
---

## Configuration

Use the `logging` entry for log configuration inside `docker-compose.yml`.

```yml
logging:
  driver: syslog
  options:
    tag: "app_service"
```

For more information about available drivers and options,
see `docker > logging`.
