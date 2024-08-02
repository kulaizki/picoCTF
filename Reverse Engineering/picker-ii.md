In this challenge, we get a Python source code that gets executed when we connect to the server.
This time, we can't simply input `win()` as we did in [Picker I](<Reverse Engineering/picker-i.md>).
Because the function `filter()` does not allow it.

```py
# picker-II.py

# ___bottom most part of the source code___

def filter(user_input):
  if 'win' in user_input:
    return False
  return True


while(True):
  try:
    user_input = input('==> ')
    if( filter(user_input) ):
      eval(user_input + '()')
    else:
      print('Illegal input')
  except Exception as e:
    print(e)(e)
```

So we can go with the alternate method of displaying the flag right after reading it using this
part of the code as reference from `win()`:

```py
flag = open('flag.txt', 'r').read()
```

<img width="1101" alt="image" src="https://github.com/user-attachments/assets/66a8749c-4355-4839-a77e-ad34e7ebfd5a">

<br>
<br>

And there we have our flag! ;D
