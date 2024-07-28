In this challenge, we get a txt file named `message.txt` and we are tasked to Take `each number mod 37 `
and map it to the following character set: `0-25 is the alphabet` (uppercase), `26-35 are the decimal digits`, 
and `36 is an underscore`.

I made this Python script to get the flag:
```py
def map_to_char(num):
  if 0 <= num <= 25:
    return chr(ord('A') + num)
  elif 26 <= num <= 35:
    return str(num - 26)
  else:
    return '_'

def main():
  numbers = input().split()
  flag = ""
  for num_str in numbers:
      num = int(num_str)
      char = map_to_char(num % 37)
      flag += char
  print(f"picoCTF{{{flag}}}")

if __name__ == "__main__":
  main()
```

Now we just have to run this and input the numbers inside `message.txt`.

<img width="963" alt="image" src="https://github.com/user-attachments/assets/4325edf5-a136-40c1-afc7-e16a81f307ea">

<br>
<br>

And there's our flag! ;)


