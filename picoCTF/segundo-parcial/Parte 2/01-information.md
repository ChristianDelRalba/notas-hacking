## Objetivo
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg)
## Pistas
PISTA 1:
Look at the details of the file
PISTA 2:
Make sure to submit the flag as picoCTF{XXXXX}
## Solución
```
Investigamos por los strings de el cat.jpg | licensee


JFIF
0Photoshop 3.0
8BIM
PicoCTF
http://ns.adobe.com/xap/1.0/
<?xpacket begin='
' id='W5M0MpCehiHzreSzNTczkc9d'?>
<x:xmpmeta xmlns:x='adobe:ns:meta/' x:xmptk='Image::ExifTool 10.80'>
<rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'>
 <rdf:Description rdf:about=''
  xmlns:cc='http://creativecommons.org/ns#'>
  <cc:license rdf:resource='cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9'/>
 </rdf:Description>
 <rdf:Description rdf:about=''
  xmlns:dc='http://purl.org/dc/elements/1.1/'>
  <dc:rights>
   <rdf:Alt>
    <rdf:li xml:lang='x-default'>PicoCTF</rdf:li>
   </rdf:Alt>
  </dc:rights>
 </rdf:Description>
</rdf:RDF>
</x:xmpmeta>
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                        
─(kali㉿kali)-[~]
└─$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}                                                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ 

picoCTF{the_m3tadata_1s_modified}    
```
## Notas adicionales

## Referencias
