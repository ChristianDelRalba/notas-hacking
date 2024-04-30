## Objetivo
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed).
## Pistas
PISTA 1:
What is the final key?

## Solución
```
chris_ap772-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed
--2024-04-30 18:38:39--  https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8888 (8.7K) [application/octet-stream]
Saving to: 'need-for-speed'

need-for-speed                            100%[===================================================================================>]   8.68K  --.-KB/s    in 0s      

2024-04-30 18:38:39 (255 MB/s) - 'need-for-speed' saved [8888/8888]

chris_ap772-picoctf@webshell:~$ chmod +x need-for-speed && ./need-for-speed
Keep this thing over 50 mph!
============================

Creating key...
Not fast enough. BOOM!
chris_ap772-picoctf@webshell:~$ gdb ./need-for-speed
GNU gdb (Ubuntu 12.1-0ubuntu1~22.04) 12.1
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from ./need-for-speed...
(No debugging symbols found in ./need-for-speed)
(gdb) handle SIGALRM ignore
Signal        Stop      Print   Pass to program Description
SIGALRM       No        No      No              Alarm clock
(gdb) r
Starting program: /home/chris_ap772-picoctf/need-for-speed 
warning: Error disabling address space randomization: Operation not permitted
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
Keep this thing over 50 mph!
============================

Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}
[Inferior 1 (process 243) exited normally]
(gdb) 




PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}
```
## Notas adicionales

## Referencias