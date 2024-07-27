In this challenge, we have `readmycert.csr`. So let's try displaying it.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/194c4c1b-705c-467a-9021-4cf62b371690">

<br>
<br>

The text inside shows an `RSA public key` in PEM-encoded data, so we can use `openssl` to extract the information
adding `req` to specify that it's for `CSR` then `-text` and `-noout` to display the extracted data as human readable text.

<img width="968" alt="image" src="https://github.com/user-attachments/assets/0974c712-32d8-4f07-a4c2-c7d17bbd84ab">

<br>
<br>

There we find our flag ;D
