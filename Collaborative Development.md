## Descripción:
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/177/challenge.zip)

# Solución
 ```bash
 MpaulaCG-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
MpaulaCG-picoctf@webshell:~/drop-in$ git branch -a
MpaulaCG-picoctf@webshell:~/drop-in$ git log
MpaulaCG-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')MpaulaCG-picoctf@webshell:~/drop-in$ $ git log feature/part-2
-bash: $: command not found
MpaulaCG-picoctf@webshell:~/drop-in$ $ git diff <commit-id> -- flag.py
-bash: commit-id: No such file or directory
MpaulaCG-picoctf@webshell:~/drop-in$ git log
MpaulaCG-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
MpaulaCG-picoctf@webshell:~/drop-in$ git log
MpaulaCG-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')MpaulaCG-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
MpaulaCG-picoctf@webshell:~/drop-in$ git log
MpaulaCG-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_7ae8dd33}")
 ```

Respuesta`picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ae8dd33}`
## Notas

## Referencias
 