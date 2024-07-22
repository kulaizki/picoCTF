In this challenge, the flag format is `picoCTF{n}` where `n` is the contents of the `eax` register 
in the decimal number base. Firstly, we are given an assembly dump.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/74e85662-9e6b-4c2e-892b-c1c86933a941">

<br>
<br>

Here we can see `DWORD PTR` **(4 bytes)** with destination address `rbp-0x4` and value `0x9fe1a`.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/752e47f5-e34a-432e-ba70-61e9a7f61fca">

<br>
<br>

This line `copies` the value of the `DWORD PTR` from the location `rbp-0x4` to the `eax` register.

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/bf67c2a7-45df-4e28-a1d4-12c2a4faffa3">
<br>
<br>

That means the value of the `eax` register is `0x9fe1a`, and we can get its decimal value using `printf`.

<img width="962" alt="image" src="https://github.com/user-attachments/assets/559ab021-d162-4f26-9c5d-8758b3b1ebb5">
<br>
<br>

So our flag would be `picoCTF{654874}` :)
