In this challenge, we are given a zip file named `unknown.zip`, so we extract it using `unzip`.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/a3b9cde5-7b05-45c1-8a52-7d1501db6711">
<br>
<br>

We get a file named `ukn_reality.jpg`, now let's try to display it using `imgcat`.

<img width="962" alt="image" src="https://github.com/user-attachments/assets/f5a1006e-46f4-4a5e-8620-5c16b21473b1">
<br>
<br>

It seems like it's just a normal image, so let's get more information about this file using `exiftool`.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/fd784b86-2ce3-43a8-bac7-2c09ac15f673">
<br>
<br>

The `Attribution URL` of this file seems to be encoded into `base64`, so let's decode that using `base64 -d`.

<img width="965" alt="image" src="https://github.com/user-attachments/assets/0c42a3b6-1915-47ba-b51c-8035314bc1e7">

And there we find the flag :)
