---
doc: https://docs.docker.com/engine/reference/commandline/image/
update: 2021-08-19
---

{% raw %}

## Usage

```shell
docker image COMMAND
```

| Command | Description |
| --- | --- |
| `ls` | List images. |
| `rm` | Remove one or more images. |
| `prune` | Remove unused images. |
| `tag` | Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE. |
| `inspect` | Display detailed information on one or more images. |
| `push` | Push an image or a repository to a registry. |
| `load` | Load an image from a tar archive or STDIN. |
| `save` | Save one or more images to a tar archive (streamed to STDOUT by default). |

## Examples

Load and save an image:

```shell
docker save imagename -o imagename.tar
docker load -i imagename.tar
```

See the creation date of an image:

```shell
docker image inspect --format '{{.Created}}' myimage
```

{% endraw %}
