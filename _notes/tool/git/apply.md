---
update: 2021-07-29
---

## Usage

Apply is used when patching.

| Option | Description |
| --- | --- |
| `-v` `--verbose` | Report progress to stderr. |
| `--check` | Only check if the patch is valid. |
| `--whitespace` | Apply an action to whitespace errors. |

### Example

```shell
git diff > mydiff.patch
git apply --whitespace=fix mydiff.patch
```
