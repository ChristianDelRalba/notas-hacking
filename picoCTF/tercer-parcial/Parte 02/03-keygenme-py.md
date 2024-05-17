## Objetivo
Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 28517`.
## Pistas
PISTA 1:
What can you do with a different pair of ciphertext and plaintext? What if it is not so different after all...

## Solución
```
──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ nano keygenme-trial.py
                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ python3 keygenme-trial.py 
Traceback (most recent call last):
  File "/home/kali/p1ex3/p2ex3/keygenme-trial.py", line 32, in <module>
    exit(key_gen())
         ^^^^^^^^^
  File "/home/kali/p1ex3/p2ex3/keygenme-trial.py", line 28, in key_gen
    for x in nums:
             ^^^^
NameError: name 'nums' is not defined. Did you mean: 'num'?
                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ nano keygenme-trial.py   
                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ python3 keygenme-trial.py
picoCTF{1n_7h3_|<3y_of_e}
picoCTF{1n_7h3_|<3y_of_e5}
picoCTF{1n_7h3_|<3y_of_e58}
picoCTF{1n_7h3_|<3y_of_e584}
picoCTF{1n_7h3_|<3y_of_e584b}
picoCTF{1n_7h3_|<3y_of_e584b3}
picoCTF{1n_7h3_|<3y_of_e584b36}
picoCTF{1n_7h3_|<3y_of_e584b363}
                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ 

```
## Notas adicionales

## Referencias


