## Objetivo
A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again.Download the message [here](https://artifacts.picoctf.net/c/182/message.txt).
## Pistas
PISTA 1:
Try a frequency attack

PISTA 2:
Do the punctuation and the individual words help you make any substitutions?

## Solución
```
Usamos wget para descargar el archivo

le hacemos un cat:

┌──(kali㉿kali)-[~/retos?examen]
└─$ cat message.txt                                     
SYTe (eakdy tkd sjbyndr yar thjm) jdr j yobr kt skxbnyrd ersndzyo skxbryzyzkc. Skcyreyjcye jdr bdrercyrq gzya j ery kt sajhhrcmre gazsa yrey yarzd sdrjyzwzyo, yrsaczsjh (jcq mkkmhzcm) evzhhe, jcq bdklhrx-ekhwzcm jlzhzyo. Sajhhrcmre nenjhho skwrd j cnxlrd kt sjyrmkdzre, jcq garc ekhwrq, rjsa ozrhqe j eydzcm (sjhhrq j thjm) gazsa ze enlxzyyrq yk jc kchzcr eskdzcm erdwzsr. SYTe jdr j mdrjy gjo yk hrjdc j gzqr jddjo kt skxbnyrd ersndzyo evzhhe zc j ejtr, hrmjh rcwzdkcxrcy, jcq jdr akeyrq jcq bhjorq lo xjco ersndzyo mdknbe jdkncq yar gkdhq tkd tnc jcq bdjsyzsr. Tkd yaze bdklhrx, yar thjm ze: bzskSYT{TD3UN3CSO_4774SV5_4D3_S001_7JJ384LS}                                                                                                                    
┌──(kali㉿kali)-[~/retos?examen]
└─$ 

y lo pasamos a esta pagina:

https://www.dcode.fr/monoalphabetic-substitution

y nos da la bandera, solo que no entra y hacemos lo siguiente:


PICOCTF{FR3JU3NCY_4774CK5_4R3_C001_7AA384BC}

Sustituimos la J por la Q:

picoCTF{FR3QU3NCY_4774CK5_4R3_C001_7AA384BC}
```
## Notas adicionales

## Referencias

https://www.dcode.fr/monoalphabetic-substitution