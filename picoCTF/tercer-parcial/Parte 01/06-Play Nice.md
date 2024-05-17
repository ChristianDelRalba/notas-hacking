## Objetivo
Not all ancient ciphers were so bad... The flag is not in standard format. `nc mercury.picoctf.net 21003` [playfair.py](https://mercury.picoctf.net/static/3329978ea3a249ef44d929b41afc5370/playfair.py)


## Solución
```
┌──(kali㉿kali)-[~]
└─$ nc mercury.picoctf.net 21003  
Here is the alphabet: 0uxtb3w4kj26q9m8gioe7nvahplr5dy1fzcs
Here is the encrypted message: xj5c181ropf5xjmyujnv0wlqrjdrbz
What is the plaintext message?                                                                                                                     
┌──(kali㉿kali)-[~]
└─$ python -c "print('TKV5Z9ZPEHCLTKQFT47NY0HMNT5LTC'.lower())"
tkv5z9zpehcltkqft47ny0hmnt5ltc
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ nc mercury.picoctf.net 21003                               
Here is the alphabet: 0uxtb3w4kj26q9m8gioe7nvahplr5dy1fzcs
Here is the encrypted message: xj5c181ropf5xjmyujnv0wlqrjdrbz
What is the plaintext message?                                                                                                                     
┌──(kali㉿kali)-[~]
└─$ tkv5z9zpehcltkqft47ny0hmnt5ltc

tkv5z9zpehcltkqft47ny0hmnt5ltc: command not found
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ nc mercury.picoctf.net 21003  
Here is the alphabet: 0uxtb3w4kj26q9m8gioe7nvahplr5dy1fzcs
Here is the encrypted message: xj5c181ropf5xjmyujnv0wlqrjdrbz
What is the plaintext message? tkv5z9zpehcltkqft47ny0hmnt5ltc
Congratulations! Here's the flag: 3f4b60ebf36369258d8638d2038c7ad1
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ 



este es la bandera:
3f4b60ebf36369258d8638d2038c7ad1
```
## Notas adicionales

## Referencias

https://www.dcode.fr/playfair-cipher
