In this challenge, we get the challenge files from `challenge.zip`.

Here we have a `SHA-256 checksum` that we can use to find the legitimate flag file.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/68277e6c-d491-4094-ae8c-297b8b16d1c2">

<br>
<br>

Now if we check the `files` directory, there are too many flag files for us to manually check
with the checksum.

<img width="934" alt="image" src="https://github.com/user-attachments/assets/13b44174-e4ae-4112-90e2-998a8b30b2e4">

<br>
<br>

We can do `sha256sum files/*` to verify which file has the same hash value, and we add `grep -f checksum.txt`
to only output the file that matches the checksum when checked with `sha256sum`.

<img width="931" alt="image" src="https://github.com/user-attachments/assets/2b1f60e7-1637-411c-8cf5-ab57c728320d">

<br>
<br>

Now we can try decrypting it using the `decrypt.sh` script.

<img width="963" alt="image" src="https://github.com/user-attachments/assets/ff2d689d-9647-4fe2-b40b-32d40db01929">

It seems like the script doesn't work properly here, and the challenge also gave us a way to connect to a server using
`ssh` in our instance to access the same files of `challenge.zip` so let's try that. In my case it's 
`ssh -p 58970 ctf-player@rhea.picoctf.net` with the password `1db87a14`.

Now that we're in the server, we can just run the same decrypt command we used before.

<img width="964" alt="image" src="https://github.com/user-attachments/assets/0c06b8f9-0bb1-44dd-8dd1-2ff83ba37ada">

<br>
<br>

And there's our flag ;)




