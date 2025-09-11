## Descripción:

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
# Solución

```bash
MpaulaCG-picoctf@webshell:~$ less level3.py 

[1]+  Stopped                 less level3.py
MpaulaCG-picoctf@webshell:~$ python3 
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import hashlib
>>> 
>>> pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
>>> 
>>> correct_pw_hash = open("level3.hash.bin", "rb").read()
>>> flag_enc = open("level3.flag.txt.enc", "rb").read()
>>> 
>>> def str_xor(secret, key):
...     new_key = key
...     i = 0
...     while len(new_key) < len(secret):
...         new_key = new_key + key[i]
...         i = (i + 1) % len(key)        
...     return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
... 
>>> def hash_pw(pw_str):
...     m = hashlib.md5()
...     m.update(pw_str.encode())
...     return m.digest()
... 
>>> for pw in pos_pw_list:
...     if hash_pw(pw) == correct_pw_hash:
...         print("[+] Contraseña correcta:", pw)
...         print("[+] Flag:", str_xor(flag_enc.decode(), pw))
...         break
... 
[+] Contraseña correcta: 865e
[+] Flag: picoCTF{m45h_fl1ng1ng_2b072a90}
```
Respuesta: picoCTF{m45h_fl1ng1ng_2b072a90}
## Notas

## Referencias
 