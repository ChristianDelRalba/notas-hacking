## Objetivo
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/29835/` ([link](https://jupiter.challenges.picoctf.org/problem/29835/)) or http://jupiter.challenges.picoctf.org:29835
## Pistas
PISTA 1:
	Never trust the client

## Solución

```

  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == '723c') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_7') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == 'e}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
    
  }

```

## Notas adicionales
Al inspeccionar el archivo nos damos cuenta en su codigo ``html`` consta de una funcion llamada ``verify`` que vendria siendo la validacion del boton, tiene un split que contiene 4 caracteres, la bandera esta desordenada, iniciamos con (0, split), luuego con (split, split*2) (split*2,split*3 )....
y se forma la contraseña en partes que ya compuesta seria:

picoCTF{no_clients_plz_7723ce}

## Referencias