---
update: 2021-08-16
---

## Usage

Make terminal-dependent capabilities and information available to the shell.

```shell
tput CAPNAME
```

| Capability name | Description |
| --- | --- |
| `bold` | Output bold text. |
| `sgr0` | Output normal text. |

## Example

```shell
echo "This text is $(tput bold)bold$(tput sgr0). This text is normal."
```
