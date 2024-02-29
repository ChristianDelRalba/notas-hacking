
## Objetivo
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)

## Pistas
PISTA 1:
On the webshell, use `ls` to see if both files are in the directory you are in
PISTA 2:
The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py
--2024-02-29 03:36:30--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.246.26, 3.160.246.109, 3.160.246.38, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.246.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                   100%[===================================================================================>]   1.25K  --.-KB/s    in 0s      

2024-02-29 03:36:31 (11.4 MB/s) - 'code.py' saved [1278/1278]

chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2024-02-29 03:36:56--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                              100%[===================================================================================>]      27  --.-KB/s    in 0s      

2024-02-29 03:36:56 (14.5 MB/s) - 'codebook.txt' saved [27/27]

chris_ap772-picoctf@webshell:~$ ls -la
total 120
drwxr-xr-x 4 chris_ap772-picoctf chris_ap772-picoctf  4096 Feb 29 03:36 .
drwxr-xr-x 3 root                root                   33 Feb 27 18:21 ..
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf  2162 Feb 29 03:35 .bash_history
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf   220 Feb 27 18:21 .bash_logout
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf  3771 Feb 27 18:21 .bashrc
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf    20 Feb 27 18:24 .lesshst
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf   807 Feb 27 18:21 .profile
drwx------ 2 chris_ap772-picoctf chris_ap772-picoctf    25 Feb 27 22:03 .ssh
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   167 Feb 27 18:23 .wget-hsts
drwxr-xr-x 3 chris_ap772-picoctf chris_ap772-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.2
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.3
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.4
-rw-r--r-- 1 root                root                 4443 Feb 29 03:36 README.txt
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    34 Mar 16  2021 flag.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   785 Mar 16  2021 ltdis.sh
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf  8376 Mar 16  2021 static
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf 10936 Mar 16  2021 warm
chris_ap772-picoctf@webshell:~$ ./code.py
-bash: ./code.py: Permission denied
chris_ap772-picoctf@webshell:~$ chmod +x code.py
chris_ap772-picoctf@webshell:~$ ./code.py
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
./code.py: line 7: syntax error near unexpected token `('
./code.py: line 7: `def str_xor(secret, key):'
chris_ap772-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}
chris_ap772-picoctf@webshell:~$ 
```
## Notas adicionales

## Referencias