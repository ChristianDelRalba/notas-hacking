## Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Pistas

PISTA 1:
Indentation is very meaningful in Python

PISTA 2:
To view the file in the webshell, do: `$ nano fixme1.py`

PISTA 3:
To exit `nano`, press Ctrl and x and follow the on-screen prompts.

PISTA 4:
The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py
--2024-02-29 04:25:12--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py.2'

fixme1.py.2           100%[=========================>]     837  --.-KB/s    in 0s      

2024-02-29 04:25:12 (37.4 MB/s) - 'fixme1.py.2' saved [837/837]

chris_ap772-picoctf@webshell:~$ ls
Addadshashanammu        Addadshashanammu.zip.3  codebook.txt  fixme1.py.1   flag.1
Addadshashanammu.zip    Addadshashanammu.zip.4  convertme.py  fixme1.py.2   ltdis.sh
Addadshashanammu.zip.1  README.txt              file          fixme1.pyM-D  static
Addadshashanammu.zip.2  code.py                 fixme1.py     flag          warm
chris_ap772-picoctf@webshell:~$ python fixme.py.2
python: can't open file '/home/chris_ap772-picoctf/fixme.py.2': [Errno 2] No such file or directory
chris_ap772-picoctf@webshell:~$ python fixme1.py.2
  File "/home/chris_ap772-picoctf/fixme1.py.2", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
chris_ap772-picoctf@webshell:~$ nano fixme1.py.2
chris_ap772-picoctf@webshell:~$ python fixme1.py.2
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales

## Referencias