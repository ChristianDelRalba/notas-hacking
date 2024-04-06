## Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)
## Pistas
PISTA 1:
Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.

## Solución

```
La pista nos dice que wireshark es la mejor herramienta para el manejo de paquetes:

abrimos el archivo con wireshark y nos da paquetes inicamos a seguir con tcp

1	0.000000	10.0.2.15	10.0.2.4	TCP	74	48750 → 9000 [SYN] Seq=0 Win=64240 Len=0 MSS=1460 SACK_PERM TSval=2379213156 TSecr=0 WS=128

Seguimos el primero y nos la bandera pero separada:

p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }

solo la juntamos y funciona la bandera.


```

## Notas adicionales

## Referencias
