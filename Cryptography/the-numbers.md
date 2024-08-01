In this challenge, we get an image file.

<img width="387" alt="the_numbers" src="https://github.com/user-attachments/assets/3038cbe5-8183-4e74-af00-c9423ed10e8b">

<br>
<br>

It seems to be in our flag, encoded in alphabet numbering (`a = 1, z = 26`). We can swiftly decode this using a Python script.
We use `chr(int(c) + 96)` to print the characters from their ascii to lowercase character format. 

```py
# alphabet.py

numbers = input().split()

for c in numbers:
    print(chr(int(c) + 96), end='')
```

Now we just have to run the script and input the numbers inside the braces `{}`.

<img width="1113" alt="image" src="https://github.com/user-attachments/assets/47c54337-75a0-4ca9-9bee-ee4040d8e077">

<br>
<br>

We get `thenumbersmason` as out output, then our flag is `picoCTF{thenumbersmason}` :)


