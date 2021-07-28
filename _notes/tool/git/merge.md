---
update: 2021-07-28
---

## Usage

Merges a source branch into the current branch.

```shell
git merge OPTIONS SOURCE_BRANCH
```

| Option | Description |
| --- | --- |
| `--squash` | Perform the merge but do not commit. |
| `--no-ff` | Force creating a merge commit. |
| `--abort` | Abort a merge with conflicts. |

### Conflict resolution

Make sure all conflicts were resolved by running:

```shell
git grep -HE '<{7} HEAD'
```

To commit with the default merge message:

```shell
git commit --no-edit
```
