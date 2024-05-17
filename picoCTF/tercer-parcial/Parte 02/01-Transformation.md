-## Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Pistas
PISTA 1:
You may find some decoders online

## Solución
```
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ wget https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc
--2024-05-17 00:26:17--  https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 57 [application/octet-stream]
Saving to: ‘enc’

enc                          100%[==============================================>]      57  --.-KB/s    in 0s      

2024-05-17 00:26:18 (69.5 MB/s) - ‘enc’ saved [57/57]

                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ cat enc        
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸強㕤㐸㤸扽                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ nano solve.py 
                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ python3 solve.py enc
Flag: picoCTF{16_bits_inst34d_of_8_75d4898b}
                                                                                                                    
┌──(kali㉿kali)-[~/p1ex3/p2ex3]
└─$ 


usamos este script llamado solve.py:

encoded_flag = open("enc").read()  
flag = ""  
for i in range(0, len(encoded_flag)):  
character1 = chr((ord(encoded_flag[i]) >> 8))  
character2 = chr(encoded_flag[i].encode('utf-16be')[-1])  
flag += character1  
flag += character2  
  
print("Flag: " + flag)

picoCTF{16_bits_inst34d_of_8_75d4898b}
```
## Notas adicionales

## Referencias

