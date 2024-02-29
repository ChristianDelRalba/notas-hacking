## Objetivo

This file has a flag in plain sight (aka "in-the-clear").
## Pistas
pista1: Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.

pista2: To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag`

pista3: `$ man cat`

## Datos de acceso al nivel
chris_ap772

## Solución

```
chris_ap772-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
--2024-02-27 18:32:29--  https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag.1'

flag.1              100%[==================>]      34  --.-KB/s    in 0s      

2024-02-27 18:32:29 (17.4 MB/s) - 'flag.1' saved [34/34]

chris_ap772-picoctf@webshell:~$ dir   
README.txt  flag  flag.1
chris_ap772-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_1a94e0f9}
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales

## Referencias