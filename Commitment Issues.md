## Descripción:
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/76/challenge.zip)

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ cd drop-in
MpaulaCG-picoctf@webshell:~/drop-in$ ls -la
total 8
drwxr-xr-x 3 MpaulaCG-picoctf MpaulaCG-picoctf   49 Mar  9  2024 .
drwxr-xr-x 4 MpaulaCG-picoctf MpaulaCG-picoctf   76 Sep 22 03:30 ..
drwxr-xr-x 8 MpaulaCG-picoctf MpaulaCG-picoctf 4096 Mar  9  2024 .git
-rw-r--r-- 1 MpaulaCG-picoctf MpaulaCG-picoctf   11 Mar  9  2024 message.txt
MpaulaCG-picoctf@webshell:~/drop-in$ git log --oneline --all
MpaulaCG-picoctf@webshell:~/drop-in$ git show e720dc2:message.txt
```

Respuesta`picoCTF{s@n1t1z3_7246792d}`

## Notas

## Referencias
 