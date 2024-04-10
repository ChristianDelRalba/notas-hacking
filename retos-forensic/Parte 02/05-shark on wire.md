## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Pistas
None

## Solución
```╠
──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ wget https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap
--2024-04-10 00:45:42--  https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 112318 (110K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                              100%[===================================================================================>] 109.69K   720KB/s    in 0.2s    

2024-04-10 00:45:43 (720 KB/s) - ‘capture.pcap’ saved [112318/112318]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ file capture.pcap 
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ wireshark capture.pcap                                                                          
python3 
                                                
^X^Z
zsh: suspended  wireshark capture.pcap
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ python3                                             
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(112)
'p'
>>> 
KeyboardInterrupt
>>> 
zsh: suspended  python3
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ nano exp.py
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ python3 exp.py 
Traceback (most recent call last):
  File "/home/kali/Desktop/PicoCTF/forensic/shark/exp.py", line 1, in <module>
    from scrapy.all import *
ModuleNotFoundError: No module named 'scrapy'
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ nano exp.py   
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/shark]
└─$ python3 exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}



Descargamos el archivo y lo analizamos con el wireshark 
vemos que hay mucho trafico de utp y lo seguimos, analizando los paquetes vemos que hay un start y un end desde 30 hasta 60 entonces hacemos un script con nano:

from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''

for p in packets:
	if UDP in p and p[UDP].dport == 22:
		if p[UDP].sport > 5000:
			flag += chr(p[UDP].sport - 5000)

print(flag)

y nos dara la bandera:

picoCTF{p1LLf3r3d_data_v1a_st3g0}

```
## Notas adicionales

## Referencias
