# Lab Report #4 (2/25/2023)
---
## CSE Labs Done Quick

---

**Logging in** 

![image](https://user-images.githubusercontent.com/81714985/221390182-a1c73b6d-4821-4482-9e4e-14a50ff77418.png)

`$ ssh cs15lwi23afn@ieng6.ucsd.edu` -> this command connects computer to the server. (used `<^C> <^V> <enter>` to copy and past from google doc)

---

**Cloning Repository** 

![image](https://user-images.githubusercontent.com/81714985/221390309-ffa05fb4-5c8f-4bba-b78b-4a5ee7b562aa.png)

`git clone git@github.com:LiamMohler/lab7.git` -> this command will clone the repository using the github link provided. (used `<^C> <^V> <enter>` to copy and past from google doc)

---

**Running Tests To See Failure** 

![image](https://user-images.githubusercontent.com/81714985/221391470-1641b4d1-0eb7-45b4-938a-2eeb5eea2c9f.png)

![image](https://user-images.githubusercontent.com/81714985/221391050-6cc893d8-ba88-4f82-8b2f-1d035f72ebae.png)


`$ ls` -> show file/directory names.

`$ cd lab7/` -> this command will enter the lab7 directory.

`$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` -> will compile all the .java files. (used `<^C> <^V> <enter>` to copy and past from google doc)

`$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` -> will run the tester file. (used `<^C> <^V> <enter>` to copy and past from google doc)


---

**Editing Code To Fix Bug** 

![image](https://user-images.githubusercontent.com/81714985/221391098-da93dbd0-9830-407a-a04e-62359cbbf7f2.png)

![image](https://user-images.githubusercontent.com/81714985/221390863-374cc042-59c2-45bd-9fde-5788b0e8e339.png)

The Error: The second while loop should add one to index2.

So change the above code to:

![image](https://user-images.githubusercontent.com/81714985/221390899-af9d10f7-0b84-4dd0-9537-905f16c548ab.png)

`$ nano ListExamples.java`-> to enter the java file to edit.

`<arrowup> <arrowdown> <del> <2>` -> to go up down, delete text, and enter in the correct number.

`<^X> <Y> <enter>` -> to exit the nano command and save edits.

---

**Running JUnit Tests... again** 

![image](https://user-images.githubusercontent.com/81714985/221391148-8162a910-cba7-46e2-9c23-ebf478ff60ee.png)

`$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` -> will compile all the .java files. (used `<^C> <^V> <enter>` to copy and past from google doc)

`$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples` -> will run the tester file. (used `<^C> <^V> <enter>` to copy and past from google doc)

The tests work this time!!!!

---

**Commiting and Pushing to GitHub** 

![image](https://user-images.githubusercontent.com/81714985/221391327-9f3d6006-d31d-4a17-84f7-8d9f1bb1bdac.png)

`$ git add ListExamples.java` -> will add the ListExamples.java file to the next commit command.

`$ git status` -> will check the status of the git commands (what files are going to be added/what file won't be).

![image](https://user-images.githubusercontent.com/81714985/221391391-7ad5479e-4e90-4dcf-8363-03bc5604694e.png)

`$ git commit -m ListExamples.java` -> will commit the file to the repository with the message "ListExamples.java"
