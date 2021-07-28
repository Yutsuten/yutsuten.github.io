---
update: 2021-07-28
---

## Usage

Change the position of HEAD.

```shell
git checkout OPTIONS BRANCH_NAME
```

| Option | Description |
| --- | --- |
| `-b` | Change to a new branch. |

### Restoring files

*Note:* If using Git 2.23 or newer,
`git restore` seems to be a more adequate command.

```shell
git checkout -- .
git checkout -- directory/
git checkout -- path/to/file

git checkout some-branch -- file
```
