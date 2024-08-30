In this challenge, we are given a zip file with a folder inside.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/e4e28662-106a-4e60-a6b3-2b31e6b1d255">
<br>
<br>

Seems like there are too many directories and files to check manually, let's try displaying all the text files here.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/1aa90ba8-43ee-46e0-9b8f-d988dbd73c05">
<br>
<br>

It still won't give us the flag, so let's use `grep -r` to recursively search for `pico` since that's our flag format.

<img width="1436" alt="image" src="https://github.com/user-attachments/assets/619844bf-a0ea-4a79-85b9-2f8ee40e8fc9">
<br>
<br>

And there we find our flag! ;D
