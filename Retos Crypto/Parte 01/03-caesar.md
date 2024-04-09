## Objetivo
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).
## Pistas
Pista 1:
caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)

## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
--2024-04-09 18:51:39--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: 'ciphertext.1'

ciphertext.1                              100%[===================================================================================>]      35  --.-KB/s    in 0s      

2024-04-09 18:51:39 (13.3 MB/s) - 'ciphertext.1' saved [35/35]

chris_ap772-picoctf@webshell:~$ cat ciphertext.1 
picoCTF{ynkooejcpdanqxeykjrbdofgkq}chris_ap772-picoctf@webshell:~$ 

Nos da esta bandera pero no es correcta, la llevamos a la pagina de rot 13, y la rotamos 4 veces esta parte:

ynkooejcpdanqxeykjrbdofgkq

y solo completamos la bandera y funciona: 

picoCTF{crossingtherubiconvfhsjkou}

```

## Notas adicionales

## Referencias
https://gchq.github.io/CyberChef/#recipe=ROT13(true,false,false,4)&input=eW5rb29lamNwZGFucXhleWtqcmJkb2Zna3E