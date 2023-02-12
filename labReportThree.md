# Lab Report #3 (2/11/2023)
---
## Researching Commands

---

**How To Grep** 

Hello, hope you're having a good day. Below are four commands to up your grep game. Oh, and here is a great [site](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) where I learned these commands from!

---
![image](https://user-images.githubusercontent.com/81714985/218286494-8526007b-015c-40ac-b864-96e6227f7d6c.png)
![image](https://user-images.githubusercontent.com/81714985/218286643-1a772da9-7b64-41e4-9e0d-c4f76b3b2657.png)
The first command is `-r` which allows the grep command to recursivly search through directories for files, in this case `*`. So essentially, this allows grep to search through directories in a specific pattern for files that contain the given string.

---

![image](https://user-images.githubusercontent.com/81714985/218286509-293dde94-2355-4d63-ac70-59fb717000b4.png)
![image](https://user-images.githubusercontent.com/81714985/218286674-a7d41dd7-09a7-4d59-a23d-21d1bf494b1d.png)

The second commmand is `-l`. This command will make it so only the file names are returned from the `grep` command. As seen above, it does not print out all the places where a certain string is found in a file, but only the files that contain the string. Making for a much more simplistic output.

---

![image](https://user-images.githubusercontent.com/81714985/218290963-596f1d91-0384-4313-a288-c02eead3fdcb.png)
![image](https://user-images.githubusercontent.com/81714985/218286708-de43a3a2-9ded-428c-a15c-cb9550f5fa67.png)

The third command, `-w`, will make sure the file contains the exact match of the text. Taking a look above, we can see that the string `"Lucayan"` can be found in both files when looking at previous images. However, that is only because `"Lucayans"` contains the substring `"Lucayan"`. When using `-w` it will ensure an exact match, so even though a text contains `"Lucayans"`, it will not say it contains `"Lucayan"`.

---

![image](https://user-images.githubusercontent.com/81714985/218286790-9ef08959-e51c-46a4-9457-a2e69d65e91a.png)
![image](https://user-images.githubusercontent.com/81714985/218286856-ca8dd07e-4ac0-4bb5-b221-5ef8473c35f2.png)

Finally, the fourth command, `-i`, ignores uppercase and lowercase discrepencies when searching for the given string. This can be seen when without the `-i` command as there is no given output (no files found). This is because without the `-i`, `grep` will search for strings that match the expression, whether that expression is a substring or not. Because it is searching for that exact match it will not check the uppercase and lowercase discrepencies. Thus this command is useful when not knowing if a word is capitalized or not. 

---
