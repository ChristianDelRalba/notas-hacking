## Objetivo

## Pistas
PISTA 1:
Try using a tool like Wireshark.
PISTA 2:
How can you decrypt the TLS stream?
## Solución
```
- descargamos el paquete y la llave
- analizamos el paquete con wireshark y vemos que la informacion que viaja por el paquete está encriptada.
- vamos a introducir la llave llendo a Edit > Preferences > Protocols > TLS > agregamos la llave.
- hacemos una busqueda de detalle de paquetes. buscamos picoCTF
- La exportamos como texto imprimible.

picoCTF{nongshim.shrimp.crackers}
```

### Solución por consola

```
[](https://github.com/azulgames/segred_ingsoft2023_SaulGamez/blob/main/Retos%20picoCTF/Retos%20Forensic/Parte%203/WebNet0.md#soluci%C3%B3n-por-consola)

```shell
┌──(kali㉿kali)-[~/Retos]
└─$ sudo apt install ssldump 

┌──(kali㉿kali)-[~/Retos] (no probado)
└─$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2

picoCTF{nongshim.shrimp.crackers}
```


## Notas adicionales

## Referencias