---
---

The `ssh-agent` manages your keys,
so you type the key file's password only once.

```shell
eval $(ssh-agent -s)

ssh-add OPTIONS PRIVATE_KEY
-l  # List
-D  # Delete
```

## Examples

```shell
ssh-add ~/.ssh/id_rsa
```

## Script

On scripts it is nice to not keep asking the user for password.

There is a way to ask only once,
then you can use the key file as much as you want.
After adding the key to the agent,
there is no need to specify the key file (`-i` argument) on subsequent ssh commands.

```shell
#!/usr/bin/ssh-agent bash
ssh-add /path/to/ssh-key
```
