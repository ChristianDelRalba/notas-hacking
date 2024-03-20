## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Datos de acceso al nivel

PISTA 1:
Try using a tool like Wireshark
PISTA 2:
What are streams?
## Solución

```
                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/extensions]
└─$ mv flag.txt flag.png
                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/extensions]
└─$ open flag.png  
                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/extensions]
└─$ cd ..        
                                                                                                                                          
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ mkdir sharkonwire1  
                                                                                                                                          
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ cd sharkonwire1 
                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/sharkonwire1]
└─$ wget https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
--2024-03-19 23:12:49--  https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 239455 (234K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                       100%[==============================================================>] 233.84K   584KB/s    in 0.4s    

2024-03-19 23:12:53 (584 KB/s) - ‘capture.pcap’ saved [239455/239455]

                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/sharkonwire1]
└─$ file capture.pcap 
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/sharkonwire1]
└─$ 


Abrimos Wireshar, que es omo un guardador de paquetes que los rastrea y nos dice a donde van y su origen, buscamos un archivo UDP Y le damos en dar seguimiento, nos muestra otra pantalla con todos ellos, y solo subimos de stream y en el 6 esta la bandera:

picoCTF{StaT31355_636f6e6e}
```

## Notas adicionales
PCAP

CUANDO ES UTIL?
para hacer analisis forenses posteriores
## Referencias
