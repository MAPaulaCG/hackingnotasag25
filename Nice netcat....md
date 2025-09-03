## Descripción:
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22342`, but it doesn't speak English...

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ cat salida.txt | python3 -c "import sys; print(''.join([chr(int(x)) for x in sys.stdin.read().split()]))"
picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}
```
Respuesta: picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}
## Notas

## Referencias