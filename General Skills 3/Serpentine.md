## Descripción:
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)

# Solución
```bash
What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) ^CTraceback (most recent call last):
  File "/home/MpaulaCG-picoctf/serpentine.py", line 80, in <module>
    main()
  File "/home/MpaulaCG-picoctf/serpentine.py", line 63, in main
    choice = input('What would you like to do? (a/b/c) ')
KeyboardInterrupt
```
Respuesta :picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
## Notas

## Referencias
 