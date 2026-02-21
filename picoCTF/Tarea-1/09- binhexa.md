### binhexa

### Descripción

How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 61628`
### Solución

### Solucion 1 - Usando Consola

```
JorgeAlamillo-picoctf@webshell:~$ nc titan.picoctf.net 61628

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01000111
Binary Number 2: 00111100


Question 1/6:
Operation 1: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10000011
Correct!

Question 2/6:
Operation 2: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00011110
Correct!

Question 3/6:
Operation 3: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10001110
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1000010100100
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01111111
Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000100
Correct!

Enter the results of the last operation in hexadecimal: 04

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6ab1ad84}

```

### Código usado para la solución de las conversiones

```
n1_bin = "01000111"
n2_bin = "00111100"

n1 = int(n1_bin, 2)
n2 = int(n2_bin, 2)

print(f"--- Resultados para N1: {n1_bin} y N2: {n2_bin} ---")

suma = n1 + n2
print(f"{bin(suma)[2:]}")

r_shift = n2 >> 1
print(f"{bin(r_shift)[2:].zfill(8)}")

l_shift = n1 << 1
print(f"{bin(l_shift)[2:]}")

multi = n1 * n2
print(f"{bin(multi)[2:]}")

op_or = n1 | n2
print(f"{bin(op_or)[2:].zfill(8)}")

op_and = n1 & n2
print(f"{bin(op_and)[2:].zfill(8)}")

print(f"{hex(op_and)[2:]}")
```