---
doc: https://docs.docker.com/engine/reference/commandline/inspect/
update: 2021-08-16
---

{% raw %}

## Usage

```shell
docker inspect OPTIONS NAME
```

| Option | Description |
| --- | --- |
| `-f` `--format` | Format the output using the given Go template. |

## Example

Output container start time and name.

```shell
docker inspect --format='{{.State.StartedAt}} {{.Name}}' NAME
```

{% endraw %}
