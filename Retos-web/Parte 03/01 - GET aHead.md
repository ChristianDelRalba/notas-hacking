## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)

## Pistas
PISTA 1:
Maybe you have more than 2 choices
PISTA 2:
Check out tools like Burpsuite to modify your requests and look at the responses

## Solución

```
Ingresamos a la pagina:
http://mercury.picoctf.net:45028/index.php

Observamos que tiene solamente dos opciones, inspeccionamos su codigo fuente y un boton manda a la base de datos como get y otro como post.

Inspeccionamos la pagina, entramos al apartado de red y presionamos el boton de "Choose Blue" nos da un post, le presionamos y vamos a darle a reenciar o resend, hacemos una nueva solicitud en el apartado y usamos HEAD, y enviamos la peticion y la respuesta es la bandera:

picoCTF{r3j3ct_th3_du4l1ty_775f2530}
```

## Notas adicionales

## Referencias