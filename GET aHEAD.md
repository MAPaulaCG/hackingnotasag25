## Descripción:
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ curl -X HEAD http://mercury.picoctf.net:45028/index.php
Warning: Setting custom HTTP method to HEAD with -X/--request may not work the 
Warning: way you want. Consider using -I/--head instead.
MpaulaCG-picoctf@webshell:~$ curl -I HEAD http://mercury.picoctf.net:45028/index.php
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8

```
Respuesta:`picoCTF{r3j3ct_th3_du4l1ty_775f2530}`
## Notas

## Referencias
 