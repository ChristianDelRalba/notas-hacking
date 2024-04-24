## Objetivo

## Pistas

PISTA 1:
Weird that it won't display right..

## Solución
```
──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ wget https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n
--2024-04-24 02:26:36--  https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2893454 (2.8M) [application/octet-stream]
Saving to: ‘tunn3l_v1s10n’

tunn3l_v1s10n                100%[==============================================>]   2.76M  1.62MB/s    in 1.7s    

2024-04-24 02:26:39 (1.62 MB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]

                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ ls -la    
total 2836
drwxr-xr-x 2 kali kali    4096 Apr 24 02:26 .
drwxr-xr-x 5 kali kali    4096 Apr 24 02:26 ..
-rw-r--r-- 1 kali kali 2893454 Mar 15  2021 tunn3l_v1s10n
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ file tunn3l_v1s10n 
tunn3l_v1s10n: data
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ xxd tunn3l_v1s10n | head
Command 'xxd' not found, but can be installed with:
sudo apt install xxd
^C   
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ exiftool tunn3l_v1s10n 
ExifTool Version Number         : 12.67
File Name                       : tunn3l_v1s10n
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2021:03:15 14:24:47-04:00
File Access Date/Time           : 2024:04:24 02:26:52-04:00
File Inode Change Date/Time     : 2024:04:24 02:26:39-04:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Unknown (53434)
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Red Mask                        : 0x27171a23
Green Mask                      : 0x20291b1e
Blue Mask                       : 0x1e212a1d
Alpha Mask                      : 0x311a1d26
Color Space                     : Unknown (,5%()
Rendering Intent                : Unknown (826103054)
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ hexeditor tunn3l_v1s10n 
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ open tunn3l_v1s10n 
                                                                                                                    
┌──(kali㉿kali)-[~/Desktop/PicoCTF/Retos-Forensic/parte03]
└─$ 


modificamos los hexadecimales de esta manera:

File: tunn3l_v1s10n                                                   ASCII Offset: 0x00000000 / 0x002C268D (%00)   
00000000  42 4D 8E 26  2C 00 00 00   00 00 28 00  00 00 28 00                                       BM.&,.....(...(.
00000010  00 00 6E 04  00 00 40 04   00 00 01 00  18 00 00 00                                       ..n...@.........
00000020  00 00 25 26  2C 00 25 16   00 00 25 16  00 00 00 00                                       ..%&,.%...%.....
00000030  00 00 00 00  00 00 23 1A   17 27 1E 1B  29 20 1D 2A                                       ......#..'..) .*
00000040  21 1E 26 1D  1A 31 28 25   35 2C 29 33  2A 27 38 2F                                       !.&..1(%5,)3*'8/
00000050  2C 2F 26 23  33 2A 26 2D   24 20 3B 32  2E 32 29 25                                       ,/&#3*&-$ ;2.2)%
00000060  30 27 23 33  2A 26 38 2C   28 36 2B 27  39 2D 2B 2F                                       0'#3*&8,(6+'9-+/
00000070  26 23 1D 12  0E 23 17 11   29 16 0E 55  3D 31 97 76                                       &#...#..)..U=1.v
00000080  66 8B 66 52  99 6D 56 9E   70 58 9E 6F  54 9C 6F 54                                       f.fR.mV.pX.oT.oT
00000090  AB 7E 63 BA  8C 6D BD 8A   69 C8 97 71  C1 93 71 C1   


y nos dara la bandera en una imagen:

picoCTF{qu1t3_a_v13w_2020}
```

## Notas adicionales

## Referencias