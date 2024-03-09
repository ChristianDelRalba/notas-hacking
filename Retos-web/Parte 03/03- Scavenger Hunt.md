
## Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:5080/](http://mercury.picoctf.net:5080/). Can you find it?
## Pistas
PISTA 1:
You should have enough hints to find the files, don't run a brute forcer.

## Solución

```
Inspeccionamos el codigo fuente:
 -En el HTML  podemos encontrar comentado la primera parte de la bandera:
 </p>
	<!-- Here's the first part of the flag: picoCTF{t -->
      </div>

    </div>

El HTML tiene un link a una hoja de estilos css:
-podemos encontrar comentada la segunda parte de la bandera: 
.tabcontent {
    color: #111;
    display: none;
    padding: 50px;
    text-align: center;
}

#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */

En este caso el JS no tiene bandera
-Regresamos al sitio original y recordamos los robots

	http://mercury.picoctf.net:5080/robots.txt

nos da la otra parte de la bandera:

User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?

Al igual que con los robots  usamos esa complementacion de un servidor apache

http://mercury.picoctf.net:5080/.htaccess

y encontramos la 4 parte de la bandera:
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information t

Nos da la pista que en las mac hay un archivo que almacena llamado DS_Store
-lo buscamos:

	http://mercury.picoctf.net:5080/.DS_Store

Nos dio la ultima parte:

Congrats! You completed the scavenger hunt. Part 5: _35844447}

flag: picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}
```


## Notas adicionales

## Referencias