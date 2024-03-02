## Objetivo
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796
## Pistas
PISTA 1:
Hmm it doesn't seem to check anyone's password, except for Joe's?

## Solución

```
`picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}`
```

## Notas adicionales

En la pagina otorgada, ingresamos, tiene un login que no nos permite entrar, ingresamos con ``admin`` y de contraseña ``hola mundo`` aunque nos dice que fuimos usuarios validos, no nos deja ver la bandera, esto por la cookie, abrimos el inspeccionador vemos las cookies, pero no nos deja modificarlas, ya que admin aparece false, y tenemos que hacerla true, descargamos un editor de cookies y vemos las cookies que pasan por el sitio, y modificamos la de admin y le ponemos de valor true y guardamos y refrescamos, y aparece la bandera.
## Referencias