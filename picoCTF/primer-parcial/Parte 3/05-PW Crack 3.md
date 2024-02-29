## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Pistas

PISTA 1:
To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
PISTA 2:
To exit `bvi` type `:q` and press enter.
PISTA 3:
The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
--2024-02-29 05:41:55--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                 100%[===================================================================================>]   1.31K  --.-KB/s    in 0s      

2024-02-29 05:41:55 (70.6 MB/s) - 'level3.py' saved [1337/1337]

chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2024-02-29 05:42:14--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                       100%[===================================================================================>]      31  --.-KB/s    in 0s      

2024-02-29 05:42:14 (9.83 MB/s) - 'level3.flag.txt.enc' saved [31/31]

chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2024-02-29 05:42:28--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                           100%[===================================================================================>]      16  --.-KB/s    in 0s      

2024-02-29 05:42:28 (167 KB/s) - 'level3.hash.bin' saved [16/16]

chris_ap772-picoctf@webshell:~$ nano level3.py
chris_ap772-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: f09e
That password is incorrect
chris_ap772-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 4dcf
That password is incorrect
chris_ap772-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
chris_ap772-picoctf@webshell:~$ ^C
chris_ap772-picoctf@webshell:~$ 
```
## Notas adicionales

Descargamos los archivos.
Con ``nano`` vemos el codigo del decodificador y vemos que en una linea aparece:

```
# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

```

Al usar la contraseña "87ab" nos arroja la bandera.

## Referencias