
## Objetivo
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/6353/` ([link](https://jupiter.challenges.picoctf.org/problem/6353/)) or http://jupiter.challenges.picoctf.org:6353
## Pistas
What is obfuscation?
## Solución
```
"picoCTF{not_this_again_50a029}"
```
## Notas adicionales

El sitio dado parece ser seguro, pero al momento de revisar su codigo fuente, vemos que nos da una funcion pero esta ofuscada, vamos a un sitio web que nos hace legibre el codigo ya desocuscado tommamos la linea:

``var _0x5a46 = ["0a029}", "_again_5", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"]  

ahora vamos a la consola de la pagina y lo pegamos y lo vamos organizando por logica

``_0x5a46 [8] + _0x5a46[9] + _0x5a46[1] + _0x5a46[0]

"picoCTF{not_this_again_50a029}"

## Referencias

http://jsnice.org/
