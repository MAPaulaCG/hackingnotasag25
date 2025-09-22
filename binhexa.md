## Descripción:
How well can you perfom basic binary operations?

Additional details will be available after launching your challenge instance

# Solución
```bash
MpaulaCG-picoctf@webshell:~/home$ nc titan.picoctf.net 49253

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10001000
Binary Number 2: 10011100


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 100010000
Correct!

Question 2/6:
Operation 2: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100100100
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01001110
Correct!

Question 4/6:
Operation 4: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10011100
Correct!

Question 5/6:
Operation 5: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10001000000
Incorrect. Try again
Enter the binary result: 101001011100000






Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 
Incorrect input. Provide the right input
Enter the binary result: 
Incorrect input. Provide the right input
Enter the binary result: 
Incorrect input. Provide the right input
Enter the binary result: 
Incorrect input. Provide the right input
Enter the binary result: 
Incorrect input. Provide the right input
Enter the binary result: 
Incorrect input. Provide the right input
Enter the binary result: 10001000
Correct!

Enter the results of the last operation in hexadecimal: 88

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}

```
Respuesta:` picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}`
## Notas

## Referencias
 