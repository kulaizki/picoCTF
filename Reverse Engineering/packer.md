In this challenge, we have to reverse this linux executable file.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/1f32578b-bd53-4747-883e-a2717f845a57">

<br>
<br>

With the challenge name being `packer` it would be a great idea to try and use a packer tool and decompress this file.
I will be using `upx -d` to decompress this.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/8b40c71b-d5e4-497d-bed3-70d9b7c72e85">

<br>
<br>

Since ELF files are usually in hex, we can use a hex editor to look into it and attempt to find the flag.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/e085ea9f-e75f-41ce-8597-9db2a2942b2e">

<br>
<br>

Now we can convert this value from hex back into binary.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/c5b59a05-5a51-464b-820d-ed4f17aa7391">

And there we find our flag! ;D
