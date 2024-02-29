## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!

## Solución

```
chris_ap772-picoctf@webshell:~$ ls
README.txt  flag  flag.1  warm
chris_ap772-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static  
--2024-02-28 14:55:14--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                          100%[======================================================================================================>]   8.18K  --.-KB/s    in 0s      

2024-02-28 14:55:14 (272 MB/s) - 'static' saved [8376/8376]

chris_ap772-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
--2024-02-28 14:55:29--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                        100%[======================================================================================================>]     785  --.-KB/s    in 0s      

2024-02-28 14:55:29 (326 MB/s) - 'ltdis.sh' saved [785/785]

chris_ap772-picoctf@webshell:~$ la
.bash_history  .bash_logout  .bashrc  .lesshst  .profile  .ssh  .wget-hsts  README.txt  flag  flag.1  ltdis.sh  static  warm
chris_ap772-picoctf@webshell:~$ ls
README.txt  flag  flag.1  ltdis.sh  static  warm
chris_ap772-picoctf@webshell:~$ chmod +x static
chris_ap772-picoctf@webshell:~$ chmod +x warm 
chris_ap772-picoctf@webshell:~$ strings static | grep pico


picoCTF{d15a5m_t34s3r_f5aeda17}
```

## Notas adicionales

## Referencias
