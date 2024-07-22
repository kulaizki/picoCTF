In this challenge, the flag format is `picoCTF{n}` where `n` is the contents of the `eax` register 
in the decimal number base. Firstly, we are given an assembly dump.

<img width="990" alt="image" src="https://github.com/user-attachments/assets/18c06ace-3b23-47e5-8d8d-f98534570d78">

<br>
<br>

This line sets the value of the EAX register to `0x30`.
```asm
<+15>:    mov    eax,0x30
```

<br>

To get the decimal value of this, we can simply use `printf` with the `%d` format specifier.

<img width="967" alt="image" src="https://github.com/user-attachments/assets/22220497-5d17-4565-b62c-1a2448014eb5">

<br>
<br>

That means our flag is `picoCTF{48}` :)
