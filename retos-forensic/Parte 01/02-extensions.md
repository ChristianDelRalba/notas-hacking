## Objetivo
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Pistas
PISTA 1:
How do operating systems know what kind of file it is? (It's not just the ending!

PISTA 2:
Make sure to submit the flag as picoCTF{XXXXX}

## Solución
```
(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/extensions]
└─$ mv flag.txt flag.png
                                                                                                                                          
┌──(kali㉿kali)-[~/…/PicoCTF/Retos-Forensic/Parte1/extensions]
└─$ open flag.png  
                                
picoCTF{now_you_know_about_extensions}
```

## Notas adicionales

Le modifficamos el tipo de archivo de texto a png, abrimos la imagen y nos dara la bandera en una imagen.

## Referencias