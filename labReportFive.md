# Lab Report #5 (3/10/2023)
---
## Going Into Detail

---

**CSE Labs Done Quicker: A CSE Labs Done Quick Parody** 

Hello, hope you're having a good day. This lab report we will break down how a bash script can turn a lab from quick to quicker!

---

**Meet The Star**

<img width="1028" alt="image" src="https://user-images.githubusercontent.com/81714985/224461044-21655fe2-5b2d-4b95-968a-baf14b4d38b8.png">

How does it work? Well, lets answer this by describing what a bash script is in the first place. A bash script is essentially a text file that contains a series of commands. Just like used for this lab, it allows one to use consecutive commands without having to type them one by one into the terminal. This is especially useful in cases where you would want to do the same process many times consecutively or quickly. Essentially automating the whole procees! Cool huh...

In this case, the first line will remove the lab7 directory if it is in the working directory. Then the other lines will clone, run tests, edit, run more tests, and commit changes to github. Wow, thats a lot. You can really see how consolidating all of these tasks into one bash script makes this process much faster.

---

**How To Set Up**

I suggest creating a new file with the `.sh` extension in VS code or some other text editor and editing it to your needs then using the `$ scp` command to copy the file into the server. Alternatively, this can all be done in the terminal using commands such as `$ touch` and `$ nano`, but I prefer the former.

<img width="1186" alt="image" src="https://user-images.githubusercontent.com/81714985/224461507-3b9c9a0b-ec56-4383-92c8-57f94935d704.png">

Now when we log into the server and use `$ ls` we should see the bash script we created.

<img width="863" alt="image" src="https://user-images.githubusercontent.com/81714985/224461748-02d52ac6-ce72-4b23-afc2-a678f8d3c8a5.png">

---

**Running The Script**

Now we're on the easy part. To run the script all you have to do is type `$ bash 'name.sh'` where name is the file name. Then bam! You're done! Told you it would turn quick to quicker. 

<img width="732" alt="image" src="https://user-images.githubusercontent.com/81714985/224462788-0349b490-a03f-4ae0-912b-1651a1ae7656.png">

<img width="684" alt="image" src="https://user-images.githubusercontent.com/81714985/224462803-34092fdb-0131-4a85-ad05-ba8e527290cb.png">
