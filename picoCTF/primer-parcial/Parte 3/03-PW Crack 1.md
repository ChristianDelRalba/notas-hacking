## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Pistas
PISTA 1:
To view the file in the webshell, do: `$ nano level1.py`
PISTA 2:
To exit `nano`, press Ctrl and x and follow the on-screen prompts.
PISTA 3:
The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py--2024-02-29 05:17:05--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py            100%[===================>]     876  --.-KB/s    in 0s      

2024-02-29 05:17:05 (39.5 MB/s) - 'level1.py' saved [876/876]

chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2024-02-29 05:17:20--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc  100%[===================>]      30  --.-KB/s    in 0s      

2024-02-29 05:17:20 (1.52 MB/s) - 'level1.flag.txt.enc' saved [30/30]

chris_ap772-picoctf@webshell:~$ ls
Addadshashanammu        code.py       fixme1.py.3          ltdis.sh
Addadshashanammu.zip    codebook.txt  fixme1.pyM-D         static
Addadshashanammu.zip.1  convertme.py  fixme2.py            strings
Addadshashanammu.zip.2  file          flag                 warm
Addadshashanammu.zip.3  fixme1.py     flag.1
Addadshashanammu.zip.4  fixme1.py.1   level1.flag.txt.enc
README.txt              fixme1.py.2   level1.py
chris_ap772-picoctf@webshell:~$ nano level1.py
chris_ap772-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
chris_ap772-picoctf@webshell:~$ ^C
chris_ap772-picoctf@webshell:~$ 
```
## Notas adicionales

descargamos los archivos, con ``nano`` abrimos el archivo de level1.py
```
if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
```
al ver esta parte del codigo vemos que la contraseña es "1e1a", ejecutamos el archivo con ``python3 level1.py`` y nos nos pedira la contraseña que vimos en el codigo, y ya nos arrojara la contraseña.
## Referencias
