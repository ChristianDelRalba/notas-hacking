
## Objetivo
Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/60915/` ([link](https://jupiter.challenges.picoctf.org/problem/60915/)) or http://jupiter.challenges.picoctf.org:60915

## Pistas
PISTA 1:
	What part of the website could tell you where the creator doesn't want you to look?

## Solución

```
picoCTF{ca1cu1at1ng_Mach1n3s_8028f}
```

## Notas adicionales

El sitio dado, no nos reporta nada, pero el creador no nos deja ver una pagina, con un archivo robots, modificamos la ruta de esta manera:

``https://jupiter.challenges.picoctf.org/problem/60915/robots.txt``

y nos da de resultado algo oculto:

``User-agent: *``
``Disallow: /8028f.html``

Volvemos a modificar el link agregandole la parte de ``8028f.html``

``https://jupiter.challenges.picoctf.org/problem/60915/8028f.html ``

## Referencias

https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es