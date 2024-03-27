
## Objetivo
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/15/challenge.zip)

Additional details will be available after launching your challenge instance.
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_atlas/15/challenge.zip
--2024-03-26 14:39:18--  https://artifacts.picoctf.net/c_atlas/15/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 741 [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                           100%[===============================================================================================================================>]     741  --.-KB/s    in 0s      

2024-03-26 14:39:18 (619 MB/s) - 'challenge.zip' saved [741/741]

edwin2809-picoctf@webshell:~$ ssh -p 62104 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:62104 ([18.217.83.136]:62104)' can't be established.
ED25519 key fingerprint is SHA256:hVmbk/OaNT4902bBr7h26wfhmBuJWi4tub8AJqoAJCM.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:62104' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
                                                                  
Se escaneo con el telefono el qr que aparece en pantalla     
ctf-player@challenge:~/drop-in$ Connection to atlas.picoctf.net closed by remote host.
Connection to atlas.picoctf.net closed.
La bandera es picoCTF{p33k_@_b00_19eccd10}
```
## Notas adicionales

## Referencias