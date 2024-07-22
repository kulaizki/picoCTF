In this challenge, we are given a strange `pdf` file named `flag2of2-final`.
When we try to open this file normally, it shows this text:

<img width="355" alt="image" src="https://github.com/user-attachments/assets/e5b42aea-72be-4b51-afee-3dd4edac6bcb">
<br>
<br>

However, it doesn't seem like a complete flag yet. So I tried getting more information
about the file by using `file`.

<img width="967" alt="image" src="https://github.com/user-attachments/assets/93943fa4-96cb-4475-997f-e3d2a454c513">

We can see that its filetype is actually `PNG`, which means there is an image inside it, and we can
display that using `imgcat`.

<img width="958" alt="image" src="https://github.com/user-attachments/assets/9d6ab2b4-6890-4a1d-8764-d1cc9d94d888">
<br>
<br>

Now it's pretty clear that we got `2/2` of our flag, which was a clever clue in the `flag2of2-final` filename. 
Combining those 2 pieces would form the actual flag which is `picoCTF{f1u3n7_1n_pn9_&_pdf_2a6a1ea8}`.

