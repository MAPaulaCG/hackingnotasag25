## Descripción:
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
--2025-09-10 16:36:04--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.72, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                         100%[======================================================================================================>]   1.25K  --.-KB/s    in 0s      

2025-09-10 16:36:04 (11.5 MB/s) - 'code.py' saved [1278/1278]

MpaulaCG-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2025-09-10 16:37:18--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.33, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                    100%[======================================================================================================>]      27  --.-KB/s    in 0s      

2025-09-10 16:37:18 (2.16 MB/s) - 'codebook.txt' saved [27/27]

MpaulaCG-picoctf@webshell:~$ python3 code.py 
picoCTF{c0d3b00k_455157_7d102d7a}
```
Respuesta:` picoCTF{c0d3b00k_455157_7d102d7a}`
## Notas

## Referencias
 