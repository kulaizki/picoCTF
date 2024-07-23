In this challenge we are given a file named `encrypted.txt`, if we try to display the text using `cat`,
It seems to be a **ROT Cipher** of the flag.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/d9d3d815-889c-4f16-9734-fbb7a9132cfd">

<br>
<br>

Since the flag format is `picoCTF{FLAG}`, we can compare `picoCTF` to `xqkwKBN`. Let's focus on `pi(c)o(C)TF`,
the `C` turned to `K` as seen in `xq(k)w(K)BN`. That means the letters have been shifted by 8, which is `ROT8`.

To decrypt this, we can use `tr` to shift the letters by 8.

<img width="963" alt="image" src="https://github.com/user-attachments/assets/c498d8fc-1469-4171-81af-c377cdd9b9ce">

And there's our flag ;>

Note: We used `A-H` in our `tr`, because `H` is the `8th` letter in the alphabet, and we need to use `ROT8`.
