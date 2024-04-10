## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Pistas
PISTA 1:
Try fixing the file header

## Solución
```
Descargamos el archivo con wget
Vemos el tipo de archivo que es tipo data, modificamos su hexadecimal con hexeditor

00000000  89 50 4E 47  0D 0A 1A 0A   00 00 00 0D  49 48 44 52                                                                                         .PNG........IHDR
00000010  00 00 06 6A  00 00 04 47   08 02 00 00  00 7C 8B AB                                                                                         ...j...G.....|..
00000020  78 00 00 00  01 73 52 47   42 00 AE CE  1C E9 00 00                                                                                         x....sRGB.......
00000030  00 04 67 41  4D 41 00 00   B1 8F 0B FC  61 05 00 00                                                                                         ..gAMA......a...
00000040  00 09 70 48  59 73 00 00   16 25 00 00  16 25 01 49                                                                                         ..pHYs...%...%.I
00000050  52 24 F0 00  00 FF A5 49   44 41 54 78  5E EC BD 3F                                                                                         R$.....IDATx^..?
00000060  8E 64 CD 71  BD 2D 8B 20   20 80 90 41  83 02 08 D0

solo se modificaron algunas y ya abrimos el archivo con open mystery y nos da la bandera en una imagen:

picoCTF{c0rrupt10n_1847995}
```
## Notas adicionales

## Referencias
