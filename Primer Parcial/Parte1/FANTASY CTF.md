## Descripción:
Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF.Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 61749`

# Solución
Primero, me conecté al servidor usando `netcat` (`nc`).

```

MpaulaCG-picoctf@webshell:~$ nc verbal-sleep.picoctf.net 61749
FANTASY CTF SIMULATION

The simulation begins in the private room of Eibhilin, a bright, young student.
The room is dimly lit, with the glow of her multiple monitors casting an
electric blue hue on the walls. Around the room are posters of vintage movies
from the MCU — ancient guardians from another age staring down like digital
sentinels.

...

```

  

El comando inició un juego de ficción interactiva que te guía a través de las reglas de picoCTF. Siguiendo la historia y tomando las decisiones correctas (como registrar una sola cuenta y jugar el juego en lugar de buscar la bandera en internet), el juego mismo te revela la bandera al final.

  

La parte final de la interacción fue la siguiente:

  

```bash
"Thanks, Nyx! Here's the flag I found: picoCTF{m1113n1um_3d1710n_219b5811}"
```

Respuesta:`"picoCTF{m1113n1um_3d1710n_219b5811}"`
## Notas

## Referencias
 