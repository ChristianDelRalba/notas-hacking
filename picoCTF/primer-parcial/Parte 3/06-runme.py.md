## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Pistas
PISTA 1:
If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.

PISTA 2:
To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'

PISTA 3:
Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!

PISTA 4:
Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now!

## Solución

```
chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2024-02-29 06:00:52--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py             100%[===================>]     270  --.-KB/s    in 0s      

2024-02-29 06:00:52 (15.1 MB/s) - 'runme.py' saved [270/270]

chris_ap772-picoctf@webshell:~$ ls
Addadshashanammu        codebook.txt  fixme2.py            level3.hash.bin
Addadshashanammu.zip    convertme.py  flag                 level3.py
Addadshashanammu.zip.1  file          flag.1               ltdis.sh
Addadshashanammu.zip.2  fixme1.py     level1.flag.txt.enc  runme.py
Addadshashanammu.zip.3  fixme1.py.1   level1.py            static
Addadshashanammu.zip.4  fixme1.py.2   level2.flag.txt.enc  strings
README.txt              fixme1.py.3   level2.py            warm
code.py                 fixme1.pyM-D  level3.flag.txt.enc
chris_ap772-picoctf@webshell:~$ python runme.py 
picoCTF{run_s4n1ty_run}
chris_ap772-picoctf@webshell:~$ ^C
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales
Descargamos el archivo python, y lo corremos con ``python runme.py`` y nos arroja la bandera.
## Referencias