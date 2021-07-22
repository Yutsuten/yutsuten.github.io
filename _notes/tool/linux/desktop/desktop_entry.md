---
doc: https://wiki.archlinux.org/title/desktop_entries
update: 2021-07-22
---

## New entry

User defined desktop entries are at `~/.local/share/applications/`.

For example, to add a desktop entry for the application `feh`,
add a file called `feh.desktop` with:

```
[Desktop Entry]
Type=Application
Name=Feh
Comment=Image viewer and cataloguer
Categories=Graphics
Exec=feh --scale-down
Terminal=0
```
