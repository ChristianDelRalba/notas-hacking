## Objetivo
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Pistas
PISTA 1:
Look up a decimal to binary number conversion app on the web or use your computer's calculator!

PISTA 2:
The `str_xor` function does not need to be reverse engineered for this challenge.

PISTA 3:
If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.

PISTA 4:
To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'

PISTA 5:
Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!

PISTA 6:
Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!

## Solución

```

chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2024-02-29 03:40:38--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                              100%[===================================================================================>]   1.16K  --.-KB/s    in 0s      

2024-02-29 03:40:38 (409 MB/s) - 'convertme.py' saved [1189/1189]

chris_ap772-picoctf@webshell:~$ ls
Addadshashanammu      Addadshashanammu.zip.1  Addadshashanammu.zip.3  README.txt  codebook.txt  flag    ltdis.sh  warm
Addadshashanammu.zip  Addadshashanammu.zip.2  Addadshashanammu.zip.4  code.py     convertme.py  flag.1  static
chris_ap772-picoctf@webshell:~$ python3 convertme.py 
If 40 is in decimal base, what is it in binary base?
Answer: 101000
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
chris_ap772-picoctf@webshell:~$ ^C
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales
El codigo python me hacia la pregunta que que numero era de decimal a binario el numero 40, le repsondi que 1010000 con ayuda de un sitio, y me entrego la bandera
## Referencias
https://es.convertbinary.com/decimal-a-binario/