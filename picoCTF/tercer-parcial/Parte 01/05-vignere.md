## Objetivo
Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/160/cipher.txt) using this key "CYLAB".
PISTA 1:
https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher


## Solución
```
Hacemos un wget para descargar el archivo, y le hacemos un cat:
y nos entrega esto:

rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_2951c89f}

nos vamos a un vignere decoder:

ponemos lo que nos dio el cat y seleccionamos la opcion de "con la clave de cifrado"

y ponemos "CYLAB"

Y nos entrega la bandera:

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}




picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}
```
## Notas adicionales

## Referencias

https://www.dcode.fr/monoalphabetic-substitution



