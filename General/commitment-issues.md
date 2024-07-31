In this challenge, we get a folder containing `message.txt`.

<img width="1122" alt="image" src="https://github.com/user-attachments/assets/a2e77d60-61f6-4b34-9ffb-665f0acbc88e">

<br>
<br>

The message doesn't seem so helpful so let's check for hidden files using `ls -la` for more info.

<img width="1123" alt="image" src="https://github.com/user-attachments/assets/89c1b4a9-acd1-40b7-8f0a-248d5dde8fa9">

<br>
<br>

Now that we found a `.git` directory, we can analyze the files here starting with the logs.

<img width="1125" alt="image" src="https://github.com/user-attachments/assets/8266320b-ebe7-47e1-befd-067727bbb1ea">

<br>
<br>

One of those commits says `create flag`, so this could be our clue. We can checkout to that commit using its `git hash`.
Additionally, we can keep using `git checkout` with `cd ..` to find the work tree we can use the command in.

<img width="1128" alt="image" src="https://github.com/user-attachments/assets/4f565d76-9367-4682-8082-ff818786dc56">

<br>
<br>

Now that we're finally in the commit, we can check the files inside it.

<img width="1133" alt="image" src="https://github.com/user-attachments/assets/3f69fc35-ec0f-4d57-ad8e-02403c12f3d5">

<br>
<br>

There we have our flag ;D







