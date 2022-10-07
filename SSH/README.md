# SSH

## Always Upgrade your server

- sudo apt install unattended-upgrades
- sudo dpkg-reconfigure --priority=low unattended-upgrades
- sudo unattended-upgrades --dry-run --debug
- ssh-keygen -b 4096 -C ""
- ssh-copy-id -i ~/.ssh/mykey user@host
- ssh-import-id gh:username
- ssh-add ~/.ssh/mykey
- useradd -m -s /bin/bash username
- usermod -aG sudo username

## Important file

- /etc/ssh/sshd_config

## Sudo Privileges

- sudo vim /etc/sudoers
- sudo visudo
- username hosts=(user:group) command_rules

## Give Certain Command Run perms

- Set the command alias

```bash
Cmnd_Alias COMMANDS = /usr/bin/ls, /usr/bin/ps
```

- Give Perms

```bash
username ALL=(ALL) NOPASSWD: COMMANDS
```

## Lock User

- sudo passwd -l username

## Unlock User

- sudo passwd -u username

## Change User Password

- sudo passwd username

## Change User Shell

- sudo chsh -s /bin/bash username

## Change User Home Dir

- sudo usermod -d /home/username username
