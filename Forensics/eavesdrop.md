In this challenge, we get a `pcap` file, and when we analyze it using `strings` we see this.

<img width="1439" alt="image" src="https://github.com/user-attachments/assets/e70f679e-4df2-41e8-88ca-44eba3765b9e">

<br>
<br>

That means we have to decrypt something, so this file might contain other files that we can decrypt, let's check
that out using `binwalk`.

<img width="949" alt="image" src="https://github.com/user-attachments/assets/198d00ca-3eea-4bf2-b9c9-76ba998e3fa8">

<br>
<br>

We found a file we can extract, so let's use `dd` or data description command to extract that file with the offset of `5882 bytes`.

<img width="682" alt="image" src="https://github.com/user-attachments/assets/24048029-fec8-46e5-a8c7-06f7eb988599">

<br>
<br>

Now we can use the decryption command shown earlier for this `bin` file, and we get a `txt` file.

<img width="1292" alt="image" src="https://github.com/user-attachments/assets/d8f4e069-44fe-4832-9be9-1f73cea5f568">

<br>
<br>

Let's look for the flag using the `picoCTF` flag format with grep.

<img width="428" alt="image" src="https://github.com/user-attachments/assets/199ea1bd-c3d0-4321-bd1c-2fc30816ce90">

<br>
<br>

And there we find our flag! ;D


