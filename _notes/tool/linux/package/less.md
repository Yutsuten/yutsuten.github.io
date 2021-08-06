---
update: 2021-08-06
---

## Usage

```shell
less OPTIONS FILE
```

| Option | Description |
| --- | --- |
| `-S` | Chop long lines |
| `-X` | Do not clean the screen |
| `-F` | Quit if one screen |
| `-R` | Show colors |
| `-N` | Show line numbers |
| `-n` | Supress line numbers |
| `+` | Automatically run commands |

It is also possible to toggle any option by typing `-` and its character.
For example, to show line numbers: `-N`.

### Commands

| Command | Description |
| --- | --- |
| `g` | Go to first line. |
| `G` | Go to last line. |
| `F` | Follow mode, `ctrl+C` to cancel. |
| `s FILENAME` | Save the input to a file. |
| `| <m>` | `<m>` represents any mark letter (`^` `$` `.`). Pipes a section of the input file to the given shell command. |
