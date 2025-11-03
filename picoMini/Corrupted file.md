## Descripción:
This file seems broken... or is it? Maybe a couple of bytes could make all the difference. Can you figure out how to bring it back to life?Download the file [here](https://challenge-files.picoctf.net/c_amiable_citadel/0165070b106635be64dc0ef9fcdd64bd1772762088a17806a3fad340de76102a/file).

# Solución

comprobamos con  xxd file | head para ver los primeros bytes en hexadecimal 
```bash
─$ xxd file | head              

00000000: 5c78 ffe0 0010 4a46 4946 0001 0100 0001  \x....JFIF......
00000010: 0001 0000 ffdb 0043 0008 0606 0706 0508  .......C........
00000020: 0707 0709 0908 0a0c 140d 0c0b 0b0c 1912  ................
00000030: 130f 141d 1a1f 1e1d 1a1c 1c20 242e 2720  ........... $.' 
00000040: 222c 231c 1c28 3729 2c30 3134 3434 1f27  ",#..(7),01444.'
00000050: 393d 3832 3c2e 3334 32ff db00 4301 0909  9=82<.342...C...
00000060: 090c 0b0c 180d 0d18 3221 1c21 3232 3232  ........2!.!2222
00000070: 3232 3232 3232 3232 3232 3232 3232 3232  2222222222222222
00000080: 3232 3232 3232 3232 3232 3232 3232 3232  2222222222222222
00000090: 3232 3232 3232 3232 3232 3232 3232 ffc0  22222222222222..

0```

Podemos ver que el problema es el archivo, es un JPEG pero los primeros 2 bytes estan mal, modificamos para parchear los dos primeros bytes para poner FFD8
```bash
┌──(kali㉿kali)-[~]


└─$ python3 - <<'PY'
data = open('file','rb').read()
open('file','wb').write(b'\xff\xd8' + data[2:])
print('patched')
PY

patched

```

Verificamos con xxd y file 
```bash
──(kali㉿kali)-[~]
└─$ xxd file | head
file file

00000000: ffd8 ffe0 0010 4a46 4946 0001 0100 0001  ......JFIF......
00000010: 0001 0000 ffdb 0043 0008 0606 0706 0508  .......C........
00000020: 0707 0709 0908 0a0c 140d 0c0b 0b0c 1912  ................
00000030: 130f 141d 1a1f 1e1d 1a1c 1c20 242e 2720  ........... $.' 
00000040: 222c 231c 1c28 3729 2c30 3134 3434 1f27  ",#..(7),01444.'
00000050: 393d 3832 3c2e 3334 32ff db00 4301 0909  9=82<.342...C...
00000060: 090c 0b0c 180d 0d18 3221 1c21 3232 3232  ........2!.!2222
00000070: 3232 3232 3232 3232 3232 3232 3232 3232  2222222222222222
00000080: 3232 3232 3232 3232 3232 3232 3232 3232  2222222222222222
00000090: 3232 3232 3232 3232 3232 3232 3232 ffc0  22222222222222..
file: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 800x500, components 3
                         

```

Finalmente comprobamos abriendo la imagen en un visor donde encontramos la flag 


Respuesta:`picoCTF{r3st0r1ng_th3_by73s_939a65f5}`

## Notas

## Referencias
 