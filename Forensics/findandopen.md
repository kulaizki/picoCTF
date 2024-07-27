In this challenge, we are given two files, `dump.pcap` and `flag.zip`. We have to find the password of
`flag.zip` inside `dump.pcap` as our trace file, so let's try to display it.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/30a8ec8d-83bc-43a8-81c1-6babfd9d8b5b">

<br>
<br>

This trace file has lots of content, but if we continue scrolling down we see that this line looks like 
it is base64 encoded since it ends with `=`.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/787c45a1-279e-4c7e-83f1-a7011634c085">

We can decode that line using `base64 -d`.

<img width="968" alt="image" src="https://github.com/user-attachments/assets/4a2f1abc-cb8a-445e-a4c8-0c99eac9a7cb">

<br>
<br>

It didn't give us anything useful after trying to decode it. However, we didn't check if it was in proper
base64 format (**string length must be a multiple of 4**). So let's count the characters in the string
using `wc`.

<img width="960" alt="image" src="https://github.com/user-attachments/assets/3fa7ae8b-6146-46ee-b3b3-2104fde0ab29">

<br>
<br>

Okay so since the length of the string is **70**, it's not a multiple of 4. We need to turn it to either 68 or 72
for it to be in the correct format. We can do that by adding two characters at the beginning of the string to make
it 72, then try decoding it again.

<img width="963" alt="image" src="https://github.com/user-attachments/assets/5ac00474-0294-4dad-91a7-97dc62bba1c7">

<br>
<br>

And there we have the password for the zip file, now we can open the zip and display the flag :D

<img width="961" alt="image" src="https://github.com/user-attachments/assets/5656de34-7bef-4e81-83a0-dc767df9ba36">


