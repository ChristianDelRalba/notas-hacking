## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Pistas
PISTA 1:
Does that encoding look familiar?
PISTA 2:
The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
chris_ap772-picoctf@webshell:~$ ls
Addadshashanammu        Addadshashanammu.zip.2  README.txt    convertme.py  fixme1.py.1  fixme1.pyM-D  flag.1               level2.flag.txt.enc  static
Addadshashanammu.zip    Addadshashanammu.zip.3  code.py       file          fixme1.py.2  fixme2.py     level1.flag.txt.enc  level2.py            strings
Addadshashanammu.zip.1  Addadshashanammu.zip.4  codebook.txt  fixme1.py     fixme1.py.3  flag          level1.py            ltdis.sh             warm
chris_ap772-picoctf@webshell:~$ python3 level2.py 
Please enter correct password for flag: 
That password is incorrect
chris_ap772-picoctf@webshell:~$ nano level2.py
chris_ap772-picoctf@webshell:~$ python3 level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
chris_ap772-picoctf@webshell:~$ ^C
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales

En el codigo de level2.py encontramos lo mismo del nivel pasado solo que la contraseña se representa en codigo hexadecimal, se hizo uso de un traductor de hexsdecimal a ascii:

```
if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
```


chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) 
 que esto se traduce a:
 chr(0x64) ->d
 chr(0x65) ->e
 chr(0x37) -> 7
 chr(0x36) -> 6

que no la pide al momento de ejecutar el archivo, y ya nos arroja la contraseña.
## Referencias
https://www.chileoffshore.com/es/toolkits/basic-conversion/hexa-to-ascii