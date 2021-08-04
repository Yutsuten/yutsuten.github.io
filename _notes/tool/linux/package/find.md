---
update: 2021-08-04
---

## Usage

```shell
find LOCATION OPTIONS
```

| Option | Description |
| --- | --- |
| `-name` | Base of file name to be matched. |
| `-type` | File type to be matched. `d` for directory, `f` for file, `l` for symbolic link. |
| `-not` `!` | Negates the next condition. |
| `-empty` | File is empty and is either a regular file or a directory. |
| `-delete` | Delete files (make sure to put it last). |
| `-print` | Print the full file name on the standard output. |

## Examples

Find files by name:

```shell
find . -name "*.js"
```

Find and delete empty directories:

```shell
find . -type d -empty -print
find . -type d -empty -delete
```

Rename multiple files (does not work if the path has spaces):

```shell
find . -type f -name 'Screenshot_*_*.png' | sed -E 'p;s/Screenshot_([0-9]{4})([0-9]{2})([0-9]{2})_([0-9]{2})([0-9]{2})([0-9]{2})([0-9]+)\.png/Screenshot_\1-\2-\3T\4:\5:\6.\7.png/g' | xargs -n 2 mv
```
