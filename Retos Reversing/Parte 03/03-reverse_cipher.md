## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this). Can you reverse the flag.
## Pistas
Pista 1:
objdump and Gihdra are some tools that could assist with this

## Solución
```
chris_ap772-picoctf@webshell:~/parte1$ wget https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev
--2024-04-30 18:28:56--  https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16856 (16K) [application/octet-stream]
Saving to: 'rev'

rev                                       100%[===================================================================================>]  16.46K  --.-KB/s    in 0s      

2024-04-30 18:28:56 (213 MB/s) - 'rev' saved [16856/16856]

chris_ap772-picoctf@webshell:~/parte1$ wget https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this
--2024-04-30 18:29:10--  https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24 [application/octet-stream]
Saving to: 'rev_this'

rev_this                                  100%[===================================================================================>]      24  --.-KB/s    in 0s      

2024-04-30 18:29:10 (12.7 MB/s) - 'rev_this' saved [24/24]

chris_ap772-picoctf@webshell:~/parte1$ ls -la
total 28
drwxrwxr-x 2 chris_ap772-picoctf chris_ap772-picoctf    33 Apr 30 18:29 .
drwxr-xr-x 6 chris_ap772-picoctf chris_ap772-picoctf  4096 Apr 30 18:28 ..
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf 16856 Oct 26  2020 rev
-rw-rw-r-- 1 chris_ap772-picoctf chris_ap772-picoctf    24 Oct 26  2020 rev_this

Hacemos un scrpit y ponemos este codigo:

cifrado = open('rev_this','r').read()
print(cifrado)

flag = ''

for i in range(8, len(cifrado)-1):
	if i & 1 == 0:
		flag += chr( ord(cifrado[i]) -5 )
	else:
		flag += chr( ord(cifrado[i]) +2 )

print(flag)

chris_ap772-picoctf@webshell:~/parte1$ nano flag.py
chris_ap772-picoctf@webshell:~/parte1$ python flag.py 
picoCTF{w1{1wq84fb<1>49}
r3v3rs36ad73964
chris_ap772-picoctf@webshell:~/parte1$ 

picoCTF{r3v3rs36ad73964}
```
## Notas adicionales

## Referencias