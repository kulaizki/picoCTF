In this challenge, we are given 2 servers to connect with using `netcat` or `nc`. If we connect to the second
server, we get this:

<img width="1125" alt="image" src="https://github.com/user-attachments/assets/c1acdfd3-1d44-48e1-8867-2151e90a2586">

<br>
<br>

Now if we connect to the first server, we get multiple questions to answer, and we get the answer to the
first question from the output of the second server. Then the others can be searched on the internet.

<img width="1123" alt="image" src="https://github.com/user-attachments/assets/4ddb3839-c071-48cf-93db-a4485e28cce0">

<br>
<br>

After correctly answering all of the questions, we get logged in as player in the server with `player@challenge`.

<img width="1123" alt="image" src="https://github.com/user-attachments/assets/cc311312-ebfe-4ef7-b070-c0368e25e996">

<br>
<br>

It seems like there's no significant information we can get from the `~` directory, then we can go and
check the `/root` directory as said in the challenge description.

<img width="1119" alt="image" src="https://github.com/user-attachments/assets/ce68b44e-2093-48bd-b69c-a9921adf776e">

<br>
<br>

Now that we're here we found `flag.txt`, but we can't access it so we can try and investigate `script.py`.

<img width="1121" alt="image" src="https://github.com/user-attachments/assets/118c55d4-3473-4a3a-ab9d-8124fc5086f4">

<br>
<br>

This is the most crucial part of the script that can help us get the flag:
```py
      with open("/home/player/banner", "r") as f:
        print(f.read())
```

It opens the file and prints the text inside, so we can use that to print the text inside `flag.txt indirectly`
and have permission. We can use symlinks to link `banner` to the path of the `flag.txt` file.

<img width="1122" alt="image" src="https://github.com/user-attachments/assets/0e6d2799-84b5-4e4c-8f79-9a0750323f8b">

Now we have to connect to the server again, so it prints the content inside `flag.txt`.

<img width="1124" alt="image" src="https://github.com/user-attachments/assets/a61224b5-6e6d-4b90-8e48-8391670064af">

And there we find our flag! ;D
