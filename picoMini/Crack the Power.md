## Descripción:
We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag.Download the [message](https://challenge-files.picoctf.net/c_amiable_citadel/f8301c52de77777b21934124245535e3672ea83b3d1976fc984c0affd45dba6f/message.txt).

# Solución
Se analizó el archivo `message.txt` 
se identificaron los valores de `n`, `e` y `c`. 
Al notar que el exponente `e = 20` era pequeño, se probó si el valor de `c` correspondía a una potencia exacta. 
Como en este caso no se aplicó reducción modular (es decir, c=m20c = m^{20}c=m20), se calculó la **raíz entera 20** de `c` para recuperar directamente el mensaje original `m`. 
Finalmente, se convirtió `m` a bytes y se decodificó en ASCII, revelando la flag.

Respuesta:`picoCTF{t1ny_e_381870dd}`
## Notas

## Referencias
 