## Objetivo
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?
## Pistas
Pista 1:
The flag is in the format PICOCTF{}

## Solución

```
Abrimos el archivo, y solo nos da numeros, sabemos que la bandera siempre inicia con picoctf entonces nos damos cuenta que esta ordenado por abecedario, sacamos los numeros:

16 9 3 15 3 20 6 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14

Nos vamos a un decodificador de numeros a letras y nos da la bandera de esta manera:

PICOCTFTHENUMBERSMASON
solo agregamos las llaves que abren y cierran:

PICOCTF{THENUMBERSMASON}

```

## Notas adicionales

## Referencias
https://www.boxentriq.com/code-breaking/a1z26