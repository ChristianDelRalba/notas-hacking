## Objetivo
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 49964`
## Solución
```
edwin2809-picoctf@webshell:~$ nc titan.picoctf.net 49964

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01000011
Binary Number 2: 01001111


Question 1/6:
Operation 1: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00100111
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10000110
Correct!

Question 3/6:
Operation 3: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01001111
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101001010101
Incorrect. Try again
Enter the binary result: 101001010101
Incorrect. Try again
Enter the binary result: 1010010101101
Correct!

Question 5/6:
Operation 5: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01000011
Correct!

Question 6/6:
Operation 6: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10010010
Correct!

Enter the results of the last operation in hexadecimal: 92

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}
```
## Notas adicionales

## Referencias
https://es.planetcalc.com/911/