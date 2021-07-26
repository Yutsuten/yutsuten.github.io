---
doc: https://wiki.archlinux.org/index.php/Rxvt-unicode
---

## Usage

```shell
urxvt
```

Use `Ctrl+Alt+C` to copy to clipboard,
`Ctrl+Alt+V` to paste from clipboard.
While selecting, right click can be used to extend selection.

## Configuration

Update its configuration by running `xrdb ~/.Xresources`.

### Font

Use `fc-list -f "%{family} : %{file}\n"` to get a full list of fonts available for use.

If you already know part of the font name,
use `fc-match 'Noto Sans Mono'`,
then it will return the best match for it.

```apiblueprint
URxvt.font: xft:Noto Sans Mono:size=9
URxvt.boldFont: xft:Noto Sans Mono:bold:size=9
URxvt.letterSpace: -1
```

Trying to fix special characters and emoji:

- [rxvt-unicode-wcwidthcallback](https://aur.archlinux.org/packages/rxvt-unicode-wcwidthcallback/)
- [nerd-fonts URxvt Known Issues](https://github.com/ryanoasis/nerd-fonts/wiki/Terminal-Emulators#urxvt)
- [wcwidth-icons](https://github.com/powerman/wcwidth-icons)

### Simple tabs

Enable the `tabbed` extension.

```apiblueprint
URxvt.perl-ext-common: tabbed
URxvt.tabbed.tabbar-fg: 10
URxvt.tabbed.tabbar-bg: 0
URxvt.tabbed.tab-fg: 2
URxvt.tabbed.tab-bg: 0
```

| Shortcut | Description |
| --- | --- |
| `Shift ↓` | New tab |
| `Shift ←` | Go to left tab |
| `Shift →` | Go to right tab |
| `Ctrl ←` | Move tab to the left |
| `Ctrl →` | Move tab to the right |
| `Ctrl d` | Close tab |

### OnTheSpot kanji conversion

Enable the `xim-onthespot` extension.

```apiblueprint
URxvt.perl-ext-common: xim-onthespot
URxvt.inputMethod: ibus
URxvt.preeditType: OnTheSpot
```
