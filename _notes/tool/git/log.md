---
doc: https://git-scm.com/docs/git-log
update: 2021-07-27
---

## Usage

Show the latest commits.

```shell
git log
git log -n 5       # Last 5 commits
git log --oneline  # Simplified output
```

Show full history of a line range.

```shell
git log -L25,+1:'path/file.txt'
```

Find a commit that deleted / edited a file.

```shell
git log --full-history -- myfile
```
