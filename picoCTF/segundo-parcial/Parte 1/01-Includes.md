## Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:61941/) and see what you can discover.

## Pistas 

PISTA 1:
Is there more code than what the inspector initially shows?


## Solución
```
Ingresamos al link del website:

http://saturn.picoctf.net:61941/

la pista nos dice que nos puede dar mas informacion el inspector de codigo

Observamos que hay un css e ingresamos y nos aparece la primer parte de la bandera:

picoCTF{1nclu51v17y_1of2_

y volvemos al codigo fuente y tambien tiene un js que nos da la segunda parte de la bandera comentada:

_6edef411}

Ingresamos la bandera y vemos que es valida:

BANDERA COMPLETA:

picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}
```

## Notas adicionales

Aprendimos a inspeccionar un codigo mas a fondo con su css y js.

## Referencias