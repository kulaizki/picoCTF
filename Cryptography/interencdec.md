In this challenge, we get the file `enc_flag.txt`.

<img width="959" alt="image" src="https://github.com/user-attachments/assets/e552717b-a4ca-42e0-aecb-e213e6bff6c5">

<br>
<br>

Since we see that this text ends with `==` it's most likely base64 encoded, let's decode it using `base64 -d`.

<img width="965" alt="image" src="https://github.com/user-attachments/assets/1844bae8-6589-4171-a845-08d5c3f194e3">

<br>
<br>

After decoding that text, it's still in base64 because it ends with `==`. Additionally, it wraps the text with `b''`
which is the format for `byte strings` in **Python**. Moreover, using the `base64 library` base64 encoded data gets 
wrapped with `b''`. So let's decode it further without including the format wrapper.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/23f79d9f-c184-4f58-b02d-85e3cc6e70da">

<br>
<br>

Now we get a text similar to picoCTF's flag format `picoCTF{FLAG}`, then it's most likely a `ROT Cipher`. If we compare
`picoCTF` and `wpjvJAM`, we can use `c` as our reference since it appears twice in `pi(c)o(C)TF` and the same goes for
`wp(j)v(J)AM` which makes it more likely to be a `ROT Cipher`. We can simply count how much we have to shift to the right 
from `c` to `j`, and that's 7 so we decode `ROT7`.

<img width="966" alt="image" src="https://github.com/user-attachments/assets/910e671d-fa1d-47b2-898d-d9dd9c55ac60">

<br>
<br>

There we have our flag! ;D

Note: we started with `h` in `tr 'h-za-gH-ZA-G' 'a-zA-Z'` because `a` shifted 7 times to the right is `h`.

