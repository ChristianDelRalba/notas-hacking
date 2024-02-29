## Objetivo

What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
## Solución

```
chris_ap772-picoctf@webshell:~$ echo "bDNhcm5fdGgzX3IwcDM1" | base64 -d
l3arn_th3_r0p35chris_ap772-picoctf@webshell:~$ 
```
BANDERA PICO: 
picoCTF{l3arn_th3_r0p35}
## Notas adicionales
usamos el comando echo y un pip para el comando ``base 64`` para que traduza el codigo de base 64 en un texto normal
## Referencias