## Objetivo
Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 9422`.
## Pistas
PISTA 1:
What kind of encoding uses dashes and dots?
PISTA 2:
The flag is in the format PICOCTF{}

## Solución
```
chris_ap772-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 9422 
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ..--- -.... ---.. ...-- ---.. ..--- ....- -.... .---- ----- } 

Traducimos el morse que nos da:
PICOCTF#M0RS3C0D31SFUN2683824610#
Solo le ponemos las llaves:
PICOCTF{M0RS3C0D31SFUN2683824610}
```
## Notas adicionales

## Referencias
https://morsedecoder.com/es/