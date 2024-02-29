## Objetivo
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)
## Pistas

PISTA 1:
Are equality and assignment the same symbol?
PISTA 2:
To view the file in the webshell, do: `$ nano fixme2.py`
PISTA 3:
To exit `nano`, press Ctrl and x and follow the on-screen prompts.
PISTA 4:
The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución

```
chris_ap772-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/5/fixme2.py
--2024-02-29 04:49:06--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py            100%[===================>]   1.00K  --.-KB/s    in 0s      

2024-02-29 04:49:06 (327 MB/s) - 'fixme2.py' saved [1029/1029]

chris_ap772-picoctf@webshell:~$ ls -la
total 936
drwxr-xr-x 5 chris_ap772-picoctf chris_ap772-picoctf   4096 Feb 29 04:49 .
drwxr-xr-x 3 root                root                    33 Feb 27 18:21 ..
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf   3295 Feb 29 04:48 .bash_history
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf    220 Feb 27 18:21 .bash_logout
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf   3771 Feb 27 18:21 .bashrc
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf  12288 Feb 29 04:24 .fixme.py.1.swp
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf     20 Feb 27 18:24 .lesshst
drwxrwxr-x 3 chris_ap772-picoctf chris_ap772-picoctf     19 Feb 29 04:11 .local
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf    807 Feb 27 18:21 .profile
drwx------ 2 chris_ap772-picoctf chris_ap772-picoctf     25 Feb 27 22:03 .ssh
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    167 Feb 29 04:36 .wget-hsts
drwxr-xr-x 3 chris_ap772-picoctf chris_ap772-picoctf     28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   4520 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   4520 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   4520 Mar 16  2021 Addadshashanammu.zip.2
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   4520 Mar 16  2021 Addadshashanammu.zip.3
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   4520 Mar 16  2021 Addadshashanammu.zip.4
-rw-r--r-- 1 root                root                  4443 Feb 29 04:48 README.txt
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf   1278 Mar 16  2023 code.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf     27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    469 Feb 29 04:20 fixme1.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    837 Mar 16  2023 fixme1.py.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    835 Feb 29 04:28 fixme1.py.2
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    835 Feb 29 04:33 fixme1.py.3
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    841 Feb 29 04:13 fixme1.pyM-D
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   1029 Mar 16  2023 fixme2.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf     34 Mar 16  2021 flag
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf     34 Mar 16  2021 flag.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    785 Mar 16  2021 ltdis.sh
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf  10936 Mar 16  2021 warm
chris_ap772-picoctf@webshell:~$ nano fixme2.py 
chris_ap772-picoctf@webshell:~$ python fixme2.py
  File "/home/chris_ap772-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
chris_ap772-picoctf@webshell:~$ nano fixme2.py 
chris_ap772-picoctf@webshell:~$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales

## Referencias
