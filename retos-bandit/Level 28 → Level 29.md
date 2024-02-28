## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
bandit28
AVanL161y9rsbcJIsFHuw35rjaOM19nR

## Solución
```

bandit28@bandit:~$ bandit28@bandit:~$  mktemp -d
/tmp/tmp.WXhQuViYYm
bandit28@bandit:~$ cd /tmp/tmp.WXhQuViYYm
bandit28@bandit:/tmp/tmp.WXhQuViYYm$ git clone ssh://bandit28-git@localhost/home/ba
ndit28-git/repo
Cloning into 'repo'...
The authenticity of host 'localhost (127.0.0.1)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server on port 22, which is not intended.

bandit28-git@localhost: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit28@bandit:/tmp/tmp.WXhQuViYYm$
```
## Notas adicionales

## Referencias
