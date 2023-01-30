# Lab Report #2 (1/29/2023)
---
## Servers and Bugs

---

**Part 1** 

<img width="200" alt="Screen Shot 2023-01-29 at 6 03 10 PM" src="https://user-images.githubusercontent.com/81714985/215373432-740f7535-7b2e-4f82-9b90-493e0361386d.png">
<img width="200" alt="Screen Shot 2023-01-29 at 6 03 40 PM" src="https://user-images.githubusercontent.com/81714985/215373441-a730d2f2-b7c2-4e3f-9734-4bc11d20ba6d.png">

In these first two images, in which the word "Hello" is added to the web page the method `handleRequest` is called as soon as the user goes to URL. The `handleRequest` method takes the given url and checks to see if it has a path. If it does, it will check to see if the path is equal to `/add`. If it is, then it will split the queury into two parts, making sure that the first part of the query is equal to `s`. Then, it will add it to a string called `str` and add a new line (`\n`). If at any point the path is not `/add` or `/`, or the first part of the query is not `s`, it will return a "404 Not Found!" error message.


<img width="400" alt="Screen Shot 2023-01-29 at 6 05 24 PM" src="https://user-images.githubusercontent.com/81714985/215373466-6c37f940-8789-42d7-a754-3a8819278708.png">
<img width="300" alt="Screen Shot 2023-01-29 at 6 05 43 PM" src="https://user-images.githubusercontent.com/81714985/215373514-e4cd88ce-f3b8-45ea-9110-3bdee5aebc69.png">

This second pair of images executes the same lines of code, in which the words "How are you" are added to the web page the method `handleRequest`. Similarly, the `handleRequest` method takes the given url and checks to see if it has a path. If it does, it will check to see if the path is equal to `/add`. If it is, then it will split the queury into two parts, making sure that the first part of the query is equal to `s`. Then, it will add it to a string called `str` and add a new line (`\n`). If at any point the path is not `/add` or `/`, or the first part of the query is not `s`, it will return a "404 Not Found!" error message. In both of these requests, the key value of `str` (which holds the string that will be displayed) is updated through this line of code:

`str += parameters[1].toString() + "\n";` -> where parameters is the array of the query split at the equals sign.



---

**Part 2** 

```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```


```
  @Test
  public void testReversed() {
    int[] input1 = { 3, 4, 6, 8};
    assertArrayEquals(new int[]{8, 6, 4, 3}, ArrayExamples.reversed(input1));
  }
```
This test case will fail because of a bug. The reversed will assign the values of arr to the values of a newArray that have not been initialized, so it will all be default int values (0). Causing the symptom of recieving the wrong output.

```
  @Test
  public void testReversed() {
    int[] input1 = { 0, 0, 0, 0};
    assertArrayEquals(new int[]{0, 0, 0, 0}, ArrayExamples.reversed(input1));
  }
```

However, running this JUnit test above will actually still give the expected output even with the bug because it will return all 0s.



<img width="849" alt="image" src="https://user-images.githubusercontent.com/81714985/215392528-35b28477-9566-47af-9a58-355bc83fe51b.png">
<img width="1018" alt="image" src="https://user-images.githubusercontent.com/81714985/215392776-9e6ef61c-31ac-479c-a301-b90168b1d4eb.png">

To fix this switch:

```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

To:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```

This will make it so the `newArray` (temp array) takes in the variables in `arr` from the last index to the front. Because we just want to return the reversed list, and not actually update `arr`, we just need to return this `newArray`, no need to update `arr` in this method. This will fix the bug because it will not assign uninitialized values of `newArray` to `arr`, but rather take the already assigned values in `arr` to create a new array (stored in `newArray`) that is reversed in order. Then returning that.

---

**Part 3** 

During week three lab this week, I was able to become more comfortable with JUnit and writing testers that actually matter. Allowing me to expand on my knowledge and understand that not all tests provide useful information. By using specifc tests that check edge cases, I can be confident in my code without having to test an infinite number of tests. All in all, during week three lab I was able to learn how to debug and test with JUnit more efficiently. 
