---
update: 2021-07-29
---

## Usage

```shell
git diff OPTIONS COMMIT -- PATH
```

| Option | Description |
| --- | --- |
| `--cached` `--staged` | Show changes in the staging area. |
| `--word-diff` | Change to show word diff mode. |
| `--stat` | Generate a diffstat. |
| `COMM1 COMM2` | Difference between two arbitrary commits. |
| `HEAD~N` | Difference between the previous commit and the working tree. |
| `HEAD~N..` `HEAD~N..HEAD` | Difference between a recent commit and the latest commit. |
| `HEAD~N..HEAD~M` | Difference between two recent commits. |

You can also use the commit's hash to specify the commit.
