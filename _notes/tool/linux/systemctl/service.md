---
doc: https://www.freedesktop.org/software/systemd/man/systemd.unit.html
update: 2021-08-11
---

## Usage

Root privileges are often needed when running `systemctl` commands.

```shell
systemctl ACTION my.service
```

| Action | Description |
| --- | --- |
| `start` | Start the service. |
| `stop` | Stop the service. |
| `restart` | Restart the service. |
| `enable` | Enable automatic service startup on boot. |
| `disable` | Disable automatic service startup on boot. |

## Creation

Services are usually placed under `/etc/systemd/system`.

Example of `someservice.service`:

```ini
[Unit]
Description=some service
Wants=network-online.target
After=network-online.target

[Service]
Type=oneshot
User=mateus
Environment=DISPLAY=:0
EnvironmentFile=/etc/someservice/someservice.conf
ExecStart=/path/to/script.py

[Install]
WantedBy=multi-user.target
```
