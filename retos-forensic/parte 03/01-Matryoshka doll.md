## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Pistas
PISTA 1:
Wait, you can hide files inside files? But how do you find them?
PISTA 2:
Make sure to submit the flag as picoCTF{XXXXX}

## Solución
```
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/parte03]
└─$ wget https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg
--2024-04-24 02:07:20--  https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651622 (636K) [application/octet-stream]
Saving to: ‘dolls.jpg’

dolls.jpg                                 100%[===================================================================================>] 636.35K  1.05MB/s    in 0.6s    

2024-04-24 02:07:24 (1.05 MB/s) - ‘dolls.jpg’ saved [651622/651622]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/parte03]
└─$ unzip dolls.jpg 
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg     
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/parte03]
└─$ ls -la
total 676
drwxr-xr-x 3 kali kali   4096 Apr 24 02:08 .
drwxr-xr-x 5 kali kali  24576 Apr 24 02:07 ..
drwxr-xr-x 2 kali kali   4096 Apr 24 02:08 base_images
-rw-r--r-- 1 kali kali 651622 Mar 15  2021 dolls.jpg
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/forensic/parte03]
└─$ cd base_images 
                                                                                                                    
┌──(kali㉿kali)-[~/…/PicoCTF/forensic/parte03/base_images]
└─$ unzip 2_c.jpg  
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg     
                                                                                                                    
┌──(kali㉿kali)-[~/…/PicoCTF/forensic/parte03/base_images]
└─$ ls -la
total 388
drwxr-xr-x 3 kali kali   4096 Apr 24 02:08 .
drwxr-xr-x 3 kali kali   4096 Apr 24 02:08 ..
-rw-r--r-- 1 kali kali 383937 Mar 15  2021 2_c.jpg
drwxr-xr-x 2 kali kali   4096 Apr 24 02:08 base_images
                                                                                                                    
┌──(kali㉿kali)-[~/…/PicoCTF/forensic/parte03/base_images]
└─$ cd base_images 
                                                                                                                    
┌──(kali㉿kali)-[~/…/forensic/parte03/base_images/base_images]
└─$ ls -la        
total 208
drwxr-xr-x 2 kali kali   4096 Apr 24 02:08 .
drwxr-xr-x 3 kali kali   4096 Apr 24 02:08 ..
-rw-r--r-- 1 kali kali 201444 Mar 15  2021 3_c.jpg
                                                                                                                    
┌──(kali㉿kali)-[~/…/forensic/parte03/base_images/base_images]
└─$ unzip 3_c.jpg 
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg     
                                                                                                                    
┌──(kali㉿kali)-[~/…/forensic/parte03/base_images/base_images]
└─$ cd base_images 
                                                                                                                    
┌──(kali㉿kali)-[~/…/parte03/base_images/base_images/base_images]
└─$ unzip 4_c.jpg 
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: flag.txt                
                                                                                                                    
┌──(kali㉿kali)-[~/…/parte03/base_images/base_images/base_images]
└─$ ls -la
total 92
drwxr-xr-x 2 kali kali  4096 Apr 24 02:09 .
drwxr-xr-x 3 kali kali  4096 Apr 24 02:09 ..
-rw-r--r-- 1 kali kali 79806 Mar 15  2021 4_c.jpg
-rw-r--r-- 1 kali kali    81 Mar 15  2021 flag.txt
                                                                                                                    
┌──(kali㉿kali)-[~/…/parte03/base_images/base_images/base_images]
└─$ cat flag.txt  
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}                                                                                                                    
┌──(kali㉿kali)-[~/…/parte03/base_images/base_images/base_images]

```
## Notas adicionales

## Referencias