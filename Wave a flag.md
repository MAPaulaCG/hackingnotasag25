## Descripción:
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
--2025-09-03 16:51:49--  https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                            100%[======================================================================================================>]  10.68K  --.-KB/s    in 0s      

2025-09-03 16:51:49 (122 MB/s) - 'warm' saved [10936/10936]

MpaulaCG-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3aa19b2a9cc4e093d64025eab8f510679b523455, with debug_info, not stripped
MpaulaCG-picoctf@webshell:~$ chmpd +x warm
-bash: chmpd: command not found
MpaulaCG-picoctf@webshell:~$ chmod +x warm
MpaulaCG-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
MpaulaCG-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
```
Respuesta: `picoCTF{b1scu1ts_4nd_gr4vy_30e77291}`
## Notas

## Referencias