In this challenge, we are given this text when we connect to the server using netcat.

<img width="1129" alt="image" src="https://github.com/user-attachments/assets/62ce593b-4b6a-46b5-9251-9151f74c38fc">

<br>
<br>

Since it's related to RSA, it's giving us a modulus `n`, encryption key `e`, and a ciphertext message `c`.
We can use this tool [RsaCtfTool](https://github.com/RsaCtfTool/RsaCtfTool) for multiple attacks using these inputs.
With the syntax `RsaCtfTool.py -e <e> -n <n> --decrypt <c>`.

<img width="1127" alt="image" src="https://github.com/user-attachments/assets/230d5336-4448-499c-8248-e49a356b970f">

<br>
<br>

It starts attempting multiple attacks on our input.

<img width="1125" alt="image" src="https://github.com/user-attachments/assets/e18fc9a6-819f-4d19-9bf1-d9bceb287c40">

<br>
<br>

And there we find our flag! ;D
