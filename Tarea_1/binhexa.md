#### Description

How well can you perfom basic binary operations?

Additional details will be available after launching your challenge instance.


How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 58655`


````

patoCosmico-picoctf@webshell:~$ nc titan.picoctf.net 58655

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10001000
Binary Number 2: 00001010


Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: ^C
patoCosmico-picoctf@webshell:~$ ^C
patoCosmico-picoctf@webshell:~$ ^C
patoCosmico-picoctf@webshell:~$ 00001000
-bash: 00001000: command not found
patoCosmico-picoctf@webshell:~$ 
patoCosmico-picoctf@webshell:~$ nc titan.picoctf.net 58655

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11001110
Binary Number 2: 11111101


Question 1/6:
Operation 1: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 111001011
Correct!

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111111
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1100101110010110
Correct!

Question 4/6:
Operation 4: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 11001110000
Incorrect. Try again
Enter the binary result: 110011100  
Correct!

Question 5/6:
Operation 5: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000000
Incorrect. Try again
Enter the binary result: 11001100
Correct!

Question 6/6:
Operation 6: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 110011.1

Incorrect input. Provide the right input
Enter the binary result: 111111.01

Incorrect input. Provide the right input
Enter the binary result: 1111110.1

Incorrect input. Provide the right input
Enter the binary result: 01111110
Correct!

Enter the results of the last operation in hexadecimal: E
Incorrect answer!

Enter the results of the last operation in hexadecimal: 7E

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d9a7ddd2}
```