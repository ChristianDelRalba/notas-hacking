## Objetivo
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.
## Pistas
PISTA 1:
Remember the flag format is picoCTF{XXXX}
PISTA 2:
What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
## Solución
```
chris_ap772-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
```

## Notas adicionales
nos conectamos a netcat con el comando ``nc`` y nos arroja demasiada informacion, para encontrar la bandera filtramos mandamos por pipe un ``grep`` con pico.


## Referencias