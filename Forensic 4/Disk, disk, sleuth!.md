## Descripción:
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz)

# Solución

```bash
MpaulaCG-picoctf@webshell:~$ zcat dds1-alpine.flag.img.gz | srch_strings -a | grep -i picoCTF

  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}
```
Respuesta`picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}`
## Notas

## Referencias
 