## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 55826`
## Pistas

PISTA 1:
ASCII is one of the most common encodings used in programming
PISTA 2:
We know that the glitch output is valid Python, somehow!
PISTA 3:
We know that the glitch output is valid Python, somehow!
## Solución

```
chris_ap772-picoctf@webshell:~$ nc saturn.picoctf.net 55826 
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
^C
chris_ap772-picoctf@webshell:~$ 
```
## Notas adicionales

Nos conectamos al servidor mediante netcat y nos proporcionala cadena con unas partes en hexadecimal.

chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) 

que esto se traduce a ascii:

ÑƁ!9..ÑƁ!c..ÑƁ!4..ÑƁ!2..ÑƁ!a..ÑƁ!4..ÑƁ!5..ÑƁ!d.

chr(0x39) -> 9
chr(0x63) -> c
chr(0x34) -> 4
chr(0x32)-> 2
chr(0x61)-> a
chr(0x34)->4
chr(0x35) -> 5
chr(0x64)-> d 

'9c42a45d'
y con esto completamos la bandera:

picoCTF{gl17ch_m3_n07_9c42a45d}


## Referencias

https://www.chileoffshore.com/es/toolkits/basic-conversion/hexa-to-ascii