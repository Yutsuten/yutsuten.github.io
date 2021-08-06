---
update: 2021-08-06
---

## Syntax

```shell
diff OPTIONS FROM_FILE TO_FILE
```

| Option | Description |
| --- | --- |
| `-y` `--side-by-side` | Output in two columns. |
| `-t` `--expand-tabs` | Expand tabs to spaces in output. |
| `-u` `-U` `--unified` | Output NUM (default 3) lines of unified context (git like). |
| `--color` | Colorize the output; Can be `never`, `always`, or `auto`. |
| `--suppress-common-lines` | Do not output common lines. |

## Examples

See the difference similarly to `git diff --no-index`.

```shell
diff -u --color=always FROM_FILE TO_FILE | less -R
```
