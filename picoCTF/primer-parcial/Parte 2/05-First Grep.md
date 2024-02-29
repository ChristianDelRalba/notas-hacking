

## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Pistas
PISTA 1:
grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)

## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
--2024-02-29 04:04:39--  https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                                      100%[===================================================================================>]  14.21K  --.-KB/s    in 0s      

2024-02-29 04:04:39 (433 MB/s) - 'file' saved [14551/14551]

chris_ap772-picoctf@webshell:~$ ls -la 
total 140
drwxr-xr-x 4 chris_ap772-picoctf chris_ap772-picoctf  4096 Feb 29 04:04 .
drwxr-xr-x 3 root                root                   33 Feb 27 18:21 ..
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf  2437 Feb 29 04:04 .bash_history
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf   220 Feb 27 18:21 .bash_logout
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf  3771 Feb 27 18:21 .bashrc
-rw------- 1 chris_ap772-picoctf chris_ap772-picoctf    20 Feb 27 18:24 .lesshst
-rw-r--r-- 1 chris_ap772-picoctf chris_ap772-picoctf   807 Feb 27 18:21 .profile
drwx------ 2 chris_ap772-picoctf chris_ap772-picoctf    25 Feb 27 22:03 .ssh
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   215 Feb 29 04:04 .wget-hsts
drwxr-xr-x 3 chris_ap772-picoctf chris_ap772-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.2
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.3
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  4520 Mar 16  2021 Addadshashanammu.zip.4
-rw-r--r-- 1 root                root                 4443 Feb 29 04:04 README.txt
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf 14551 Oct 26  2020 file
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    34 Mar 16  2021 flag.1
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf   785 Mar 16  2021 ltdis.sh
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf  8376 Mar 16  2021 static
-rwxrwxr-x 1 chris_ap772-picoctf chris_ap772-picoctf 10936 Mar 16  2021 warm
chris_ap772-picoctf@webshell:~$ cat file | grep pico
picoCTF{grep_is_good_to_find_things_f77e0797}
chris_ap772-picoctf@webshell:~$ 
```

## Notas adicionales
 descargamos el archivo y con el comando ``cat`` lo leemos pero lo pasamos por pip al comando ``grep`` para buscar la linea en la que aparece 'pico' para obtener la contraseña.

## Referencias