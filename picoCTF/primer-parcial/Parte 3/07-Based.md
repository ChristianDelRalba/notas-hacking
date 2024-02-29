## Objetivo
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.
## Pistas
PISTA 1:
I hear python can convert things.
PISTA 2:
It might help to have multiple windows open.
## Solución

```
chris_ap772-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130 
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
falcon
Please give me the  146 141 154 143 157 156 as a word.
Input:
falcon
Please give me the 7375626d6172696e65 as a word.
Input:
submarine
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}

```

## Notas adicionales
Al momento de iniciar el link con ``nc`` nos arroja que le demos este numero binario en texto: 
 
 01100110 01100001 01101100 01100011 01101111 01101110 
que significa falcon, es correcta, luego nos da un numero octal 
146 141 154 143 157 156
que significa igual falcon fue de octal a texto, por ultimo nos da un numero hexadecimal: 
7375626d6172696e65
que significaba submarine y ya nos otorga la bandera.

## Referencias
https://www.rapidtables.com/convert/number/binary-to-ascii.html
http://www.unit-conversion.info/texttools/octal/
https://www.rapidtables.com/convert/number/hex-to-ascii.html