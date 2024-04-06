## Objetivo
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:63773/) out.
## Pistas


## Solución
```
Nos dice la descripcion que no esta la bandera necesariamente en el sitio
Revise su codigo fuente y solo encontre un comentario que dice:

The flag is not here but keep digging :)-- >

y seguimos revisando, sus js, css, jpg y nada, recorde el metodo de robots que era de un reto anterior, donde editabamos la direccion de esta manera:

view-source:http://saturn.picoctf.net:63773/robots.txt

solo nos da esto:
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

decodificamos esta parte en base 64:

anMvbXlmaWxlLnR4dA==

nos da esto: 
js/myfile.txt

Ahora copiamos eso a la direccion del sitio:

view-source:http://saturn.picoctf.net:63773/js/myfile.txt

Y nos dara la bandera:

picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}




```
## Notas adicionales

## Referencias
