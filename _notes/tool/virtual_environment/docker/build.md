---
doc: https://docs.docker.com/engine/reference/commandline/build/
update: 2021-08-18
---

## Usage

```shell
docker build OPTIONS CONTEXT
```

| Option | Description |
| --- | --- |
| `-f` `--file` | Path to the Dockerfile. |
| `-t` `--tag` | Name and optionally tag in the 'name:tag' format. |
| `--no-cache` | Do not use cache when building the image. |
| `--pull` | Always attempt to pull a newer version of the image. |

## Example

Build using the current directory as context and a custom `Dockerfile`.

```shell
docker build -f dockerfile/prod -t custom.registry:4567/imagename:latest .
```
