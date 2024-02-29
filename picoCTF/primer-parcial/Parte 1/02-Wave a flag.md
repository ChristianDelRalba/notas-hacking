## Objetivo

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
## Datos de acceso al nivel

## Solución
 ```
 chris_ap772-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
--2024-02-27 18:34:00--  https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                            100%[======================================================================================================>]  10.68K  --.-KB/s    in 0s      

2024-02-27 18:34:00 (222 MB/s) - 'warm' saved [10936/10936]

chris_ap772-picoctf@webshell:~$ chmod +x warm
chris_ap772-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
chris_ap772-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales

## Referencias