In this challenge, the flag format is `picoCTF{n}` where `n` is the contents of the `eax` register 
in the decimal number base. Firstly, we are given an assembly dump.

<img width="990" alt="image" src="https://github.com/user-attachments/assets/880fecbd-b159-44dc-9f18-1b06e66fd362">
<br>
<br>

These lines store values into their specific `32-bit memory locations`. 

<img width="991" alt="image" src="https://github.com/user-attachments/assets/e5c745ce-2ea5-45d3-bbb3-de7ff58930ea">

`0x9fe1a` into `rbp-0xc` and `0x4` into `rbp-0x8`.
<br>
<br>

This line loads the `DWORD PTR` from `rbp-0xc` into the `eax` register.

<img width="973" alt="image" src="https://github.com/user-attachments/assets/c0f4cb9c-1979-482b-aa2d-bb98897f9cb5">
<br>
<br>

Now in these two lines, we do arithmetic operations. `imul` **(signed multiply)** multiplies the value
of the `eax` by the value of the `DWORD PTR` in location `rbp-0x8` and then adds `0x1f5` to the value of 
the `eax`.

<img width="984" alt="image" src="https://github.com/user-attachments/assets/5231e6dc-52bf-4002-9953-332d04f8300e">
<br>
<br>

The expression with the arithmetic operations should be equivalent to `0x9fe1a * 0x4 + 0x1f5`. Now let's get
the decimal value of that using `printf`.

<img width="970" alt="image" src="https://github.com/user-attachments/assets/417ddadf-6a3a-483c-8a0c-7009c9642ccc">
<br>
<br>

That means our flag is `picoCTF{2619997}` ;D



