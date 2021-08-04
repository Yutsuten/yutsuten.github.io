---
update: 2021-08-04
---

## Usage

```shell
tar OPTIONS SOURCE
```

On options, hyphen is optional.

| Option | Description |
| --- | --- |
| `-c` `--create` | Create tar file. |
| `-x` `--extract` `--get` | Extract tar file. |
| `-t` `--list` | List the contents of an archive. |
| `-C` `--directory` | Set current directory. |
| `-f` `--file` | Set the name of the file to create / extract. |
| `-z` `--gzip` `--gunzip` `--ungzip` | Enable gnuzip. |
| `-v` `--verbose` | Verbosely list files processed. |

Gzipped files can have `.tgz` or `.tar.gz` extensions.

## Examples

Compress a folder:

```shell
tar -cf grouped.tar myfolder   # Create File
tar -czf grouped.tgz myfolder  # Create Gzipped File
```

Extract gzipped file:

```shell
tar -xzf file.tgz
```

List files in tar file:

```shell
tar -tf file.tar
```
