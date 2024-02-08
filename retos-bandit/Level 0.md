## Objetivo
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is *bandit.labs.overthewire.org, on port 2220. The username is **bandit0* and the password is *bandit0*. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.
## Datos de acceso al nivel
username: bandit0
password: bandit0
## Solución

```
C:\Users\Chris\.ssh>ssh bandit0@bandit.labs.overthewire.org -p 2220
The authenticity of host '[bandit.labs.overthewire.org]:2220 ([51.20.13.48]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[bandit.labs.overthewire.org]:2220' (ED25519) to the list of known hosts.
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password:
```

## Notas adicionales
- Ssh es un protocolo seguro para conexiones en internet
- Como conectarnos con el ssh
## Referencias

- [Shell seguro (SSH) en Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [Cómo usar SSH en wikiHow](https://www.wikihow.com/Use-SSH)