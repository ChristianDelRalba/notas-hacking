## Objetivo
Morse code is well known. Can you decrypt this?Download the file [here](https://artifacts.picoctf.net/c/79/morse_chal.wav).Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase.
## Pistas
PISTA 1:
Audacity is a really good program to analyze morse code audio.

## Solución
```
Descargamos el audio que esta en el link

ahora buscamos en google un decodificador de audio morse

subimos el audio y nos empieza a decodificarlo, nos da esto:

WH47 H47H 90D W20U9H7

y solo agregamos guin bajo y las mayusculas a minusculas y sale la bandera agregando picoCTF{}:

picoCTF{wh47_h47h_90d_w20u9h7}
```
## Notas adicionales

## Referencias

https://morsecode.world/international/decoder/audio-decoder-adaptive.html