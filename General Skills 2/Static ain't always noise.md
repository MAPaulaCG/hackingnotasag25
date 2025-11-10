## Descripción:
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!


# Solución
```bash
MpaulaCG-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
--2025-09-03 17:02:59--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                          100%[======================================================================================================>]   8.18K  --.-KB/s    in 0s      

2025-09-03 17:02:59 (280 MB/s) - 'static' saved [8376/8376]

MpaulaCG-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
--2025-09-03 17:03:27--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                        100%[======================================================================================================>]     785  --.-KB/s    in 0s      

2025-09-03 17:03:27 (314 MB/s) - 'ltdis.sh' saved [785/785]

MpaulaCG-picoctf@webshell:~$ ls
README.txt  ltdis.sh  static
MpaulaCG-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_f5aeda17}
```
Respuesta: `picoCTF{d15a5m_t34s3r_f5aeda17}`
## Notas

## Referencias