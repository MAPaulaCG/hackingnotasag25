## Descripción:
#### Description

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)

# Solución
```bash
clcMpaulaCG-picoctf@webshell:~$ python3 fixme1.py 
  File "/home/MpaulaCG-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
MpaulaCG-picoctf@webshell:~$ nano fixme1.py 
MpaulaCG-picoctf@webshell:~$ nano fixme1.py 
MpaulaCG-picoctf@webshell:~$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
Respuesta: `picoCTF{1nd3nt1ty_cr1515_6a476c8f}`


## Notas

## Referencias
 