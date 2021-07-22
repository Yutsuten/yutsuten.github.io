---
doc: https://wiki.archlinux.org/title/XDG_MIME_Applications
update: 2021-07-22
---

## Usage

To change the default application of a certain file:

```shell
xdg-mime default feh.desktop image/jpeg
```

The configuration is saved at `~/.config/mimeapps.list`.

To open a file using the default application:

```shell
xdg-open file.jpg
```
