---
doc: https://git-scm.com/docs/git-log
update: 2021-07-29
---

## Usage

Show the latest commits.

```shell
git log OPTIONS
```

| Option | Description |
| --- | --- |
| `-n` | Output only the last N commits. |
| `-L` | Get the logs of the given line range and file. |
| `--oneline` | Abbreviate commit messages to one line. |
| `--merges` | Output only merge commits. |
| `--full-history` | Do not prune some history. |

### Examples

Show full history of a line range.

```shell
git log -L25,+1:'path/file.txt'
```

Find a commit that deleted / edited a file.

```shell
git log --full-history -- myfile
```
