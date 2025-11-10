## Descripción:
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
pie
Please give the 01110000 01101001 01100101 as a word.
...
you have 45 seconds.....

Input:
pie
Please give me the  154 141 155 160 as a word.
Input:
lamp
Please give me the 6c697a617264 as a word.
Input:
lizard
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}
```
Respuesta: `picoCTF{learning_about_converting_values_02167de8}`
## Notas
Usamos cyberchef
## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Hex('None')&input=NmM2OTdhNjE3MjY0