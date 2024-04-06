## Objetivo

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 49602 -U postgres pico`Password is `postgres`

## Pistas
PISTA 1:
What does a SQL database contain?

## Solución
```
Abrimos linux, ingresamos el link de psql y funciona, ingresamos la contraseña que es: postgres

ingresamos e intentamos ver las tablas con "\dt" y nos da un directorio buscamos con el 

SELECT * FROM flags

y nos da la bandera. de esta manera es en codigo:

┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 49602 -U postgres pico
Password for user postgres: 
psql (16.1 (Debian 16.1-1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 

```
## Notas adicionales

## Referencias
https://www.postgresqltutorial.com/postgresql-administration/postgresql-show-tables/


