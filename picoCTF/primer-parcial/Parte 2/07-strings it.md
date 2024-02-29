## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
## Pistas
PISTA 1:
strings
## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2024-02-29 04:36:18--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                   100%[===================================================================================>] 757.84K  1.83MB/s    in 0.4s    

2024-02-29 04:36:18 (1.83 MB/s) - 'strings' saved [776032/776032]

chris_ap772-picoctf@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  Addadshashanammu.zip.3  README.txt  codebook.txt  file       fixme1.py.1  fixme1.py.3   flag    ltdis.sh  strings
Addadshashanammu.zip  Addadshashanammu.zip.2  Addadshashanammu.zip.4  code.py     convertme.py  fixme1.py  fixme1.py.2  fixme1.pyM-D  flag.1  static    warm
chris_ap772-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}
chris_ap772-picoctf@webshell:~$ 
```
## Notas adicionales

con el comando strings abrimos el texto ejecutable y lo pasamos por pip a un grep para filtrar la contraseña que comienza por 'pico'.

## Referencias
