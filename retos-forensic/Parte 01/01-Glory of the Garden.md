## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.
## Pistas
Pista 1:
What is a hex editor?
## Solución

```
┌──(kali㉿kali)-[~]
└─$ cd Desktop 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir PicoCTF
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop]
└─$ cd PicoCTF 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF]
└─$ mkdir Retos-Forensic
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF]
└─$ cd Retos-Forensic   
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic]
└─$ mkdir Parte1        
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic]
└─$ cd Parte1        
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ mkdir 01    
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ wget https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg  
--2024-03-19 15:35:53--  https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg                                 52%[===========================================>                                        ]   1.16M   328KB/s    eta 4s     ^garden.jpg                                 56%[==============================================>                                     ]   1.23M   329KB/s    eta 4s     ^garden.jpg                                100%[===================================================================================>]   2.19M   214KB/s    in 8.4s    

2024-03-19 15:36:04 (266 KB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ ls    
01  garden.jpg
                                                                                                                                          
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ file garden.jpg 
garden.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, baseline, precision 8, 2999x2249, components 3
                                                                                                                                          
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ open garden.jpg 
                                                                                                                                          
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ hexeditor garden.jpg 
                                                                                                                                          
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/Parte1]
└─$ strings garden.jpg 

Nos da todas las cadenas que hay dentro del archivo, al final tenemos la bandera.

picoCTF{more_than_m33ts_the_3y3eBdBd2cc}
```
## Notas adicionales

## Referencias

https://es.wikipedia.org/wiki/Editor_hexadecimal