## Descripción:
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-09-10 16:31:35--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.18, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                        100%[======================================================================================================>]     270  --.-KB/s    in 0s      

2025-09-10 16:31:35 (10.3 MB/s) - 'runme.py' saved [270/270]

MpaulaCG-picoctf@webshell:~$ python3 runme.py
picoCTF{run_s4n1ty_run}
```

## Notas

## Referencias
 