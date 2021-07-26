---
doc: https://www.hanselman.com/blog/the-easy-way-how-to-ssh-into-bash-and-wsl2-on-windows-10-from-an-external-machine
update: 2021-07-26
---

## Setup using Windows openssh

With this setup,
it is Windows who will manage the login into the WSL2.

First open the Power Shell as admin,
install and start SSH server.

```powershell
Get-WindowsCapability -Online | ? Name -like 'OpenSSH*'
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
Start-Service sshd
Get-Service sshd
Set-Service -Name sshd -StartupType 'Automatic'
```

Then set the default shell for when logging with SSH.
Choose `bash.exe` to run WSL2 with bash,
or `wsl.exe` to run the default shell set in Linux.

```powershell
New-ItemProperty -Path "HKLM:\SOFTWARE\OpenSSH" -Name DefaultShell -Value "C:\WINDOWS\System32\bash.exe" -PropertyType String -Force
New-ItemProperty -Path "HKLM:\SOFTWARE\OpenSSH" -Name DefaultShell -Value "C:\Windows\System32\wsl.exe" -PropertyType String -Force
```

To get the IP address to be used in the SSH command:

```powershell
ipconfig /all
```

Remember that when logging in,
the username and password will be the of the Windows account,
not the Linux one.

```shell
ssh mywinuser@192.168.0.107
```

If you chose `wsl.exe` in the steps above,
set your default shell inside WSL2.

```shell
sudo chsh -s $(which zsh)
```

Seems that with this setup X11 forwarding does not work.
More setup may be needed.

## Setup using Linux openssh

The steps here are incomplete.

Install `openssh-server` and start the server.

```shell
sudo apt install openssh-server
sudo service ssh start
```

Seems that it defaults to using a key file.
Change this in `/etc/ssh/sshd_config`:

```
PasswordAuthentication yes
```

Then restart the ssh service.

```shell
sudo service ssh restart
```
