In this challenge, we get a Python source code that gets executed when we connect to the server.
It takes input and uses `eval()` on the input to execute a function inside the code.

```py
# picker-I.py

# ___bottom most part of the source code___

while(True):
  try:
    print('Try entering "getRandomNumber" without the double quotes...')
    user_input = input('==> ')
    eval(user_input + '()') 
  except Exception as e:
    print(e)
```

Let's try connecting to the server.

<img width="1100" alt="image" src="https://github.com/user-attachments/assets/a5315b47-6f98-44d6-b754-70c2f0e00f6a">

<br>
<br>

It successfully ran a function inside the code. And if we check the source code there's this function named `win()`.
That function seems to give us our flag.

```py
def win():
  # This line will not work locally unless you create your own 'flag.txt' in
  #   the same directory as this script
  flag = open('flag.txt', 'r').read()
  #flag = flag[:-1]
  flag = flag.strip()
  str_flag = ''
  for c in flag:
    str_flag += str(hex(ord(c))) + ' '
  print(str_flag)
```

So let's try executing it from the server.

<img width="1101" alt="image" src="https://github.com/user-attachments/assets/f3254493-02d2-4b12-9cd7-88d21484d269">

<br>
<br>

We are given hex values of ASCII characters, and we can simply convert them to characters by inputting the hex values 
into this Python script.

```py
# hex.py

hex_string = "0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x63 0x65 0x34 0x62 0x35 0x64 0x35 0x62 0x7d"

hex_values = hex_string.split()

flag = ''.join([chr(int(c, 16)) for c in hex_values])
print(flag)
```

Now let's run that script.

<img width="1101" alt="image" src="https://github.com/user-attachments/assets/df358943-0002-4769-8e61-dc1e83de5a8e">

<br>
<br>

And there we have our flag! ;D


