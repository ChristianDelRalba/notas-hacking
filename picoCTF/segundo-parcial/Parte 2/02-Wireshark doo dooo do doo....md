## Objetivo

Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ae5b2bc07928fca272ff3900dc9a6cef/shark1.pcapng).
## Pistas


## Solución
```
Una de las cosas es descargar wireshark
Nos da un archivo lo descargamos y abrimos, se abre el wireshark y buscamos el get

823	7.187055	192.168.38.104	18.222.37.134	HTTP	501	GET / HTTP/1.1 

Le damos seguir http:

y nos da esto: 

GET / HTTP/1.1

Host: 18.222.37.134

Connection: keep-alive

Cache-Control: max-age=0

Upgrade-Insecure-Requests: 1

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9

Accept-Encoding: gzip, deflate

Accept-Language: en-US,en;q=0.9

  

HTTP/1.1 200 OK

Date: Mon, 10 Aug 2020 01:51:45 GMT

Server: Apache/2.4.29 (Ubuntu)

Last-Modified: Fri, 07 Aug 2020 00:45:02 GMT

ETag: "2f-5ac3eea4fcf01"

Accept-Ranges: bytes

Content-Length: 47

Keep-Alive: timeout=5, max=100

Connection: Keep-Alive

Content-Type: text/html

  

Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}

esta parte nos interesa:

cvpbPGS{c33xno00_1_f33_h_qrnqorrs}

Nos vamos a un decodificador de rot13

y nos da la bandera:

picoCTF{p33kab00_1_s33_u_deadbeef}
```

## Notas adicionales

## Referencias

https://rot13.com/