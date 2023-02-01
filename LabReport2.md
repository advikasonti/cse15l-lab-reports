# Lab Report 2

##  Servers and Bugs

### Part 1: StringServer

For tis lab, I created a StringServer class that suppports the path and behavior of keeping track of a single string that gets added to by incoming requests. Here is my code for the method that does this:

![Code.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Code.png)

I then launched the localhost and played around with the possible requests. For the screenshots below, the handRequest method (for which I poseted the code above) is what is called. The add-message value is given at the end of the URL, which allows the query to follow. The complete request then looks like `/add-message?s=` followed by the String to be added. In the latter screenshots, you can then see how the next String requests are added to the existing String to be displayed on a new line each time.

![Message1.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Message1.png)

![Message2.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Message2.png)

![Message3.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Message3.png)

Lastly, I tried to make an `/add-message?` request without properly adding the `s=` query format, which resulted in an error message as it was supposed to. 

![NotFound.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/NotFound.png)

### Part 2: Array Bugs

Failure-inducing input for the buggy program:
```
@Test
  public void testReverseInPlaceNew() {
    int[] input1 = {2,1,5,3,4};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{4,3,5,1,2}, input1);
  }
  ```
  
  The symptom:
  
  ![Symptom1.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Symptom1.png)
  
 Input that passes the buggy program:
 ```
@Test 
  public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
  }
  ```
  
  The symptom:
  
  ![Symptom2.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Symptom2.png)
  
  Code before (with bug):
  ```
   static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  ```
  
  Code after (fixed bug):
  ```
   static void reverseInPlace(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[i];
    }
  } 
  ```
  
The bug was that the reverseInPlace method, in the initial version, would replace the values in the array as it was reversing it. This caused the method to only reverse half of the array such that first half became a reflection of the second half of the array. To fix this bug, I just changed the program to reverse the entire given array into a new array such that none of the values of the given array are lost. Then I simply set the original array to the new one after the complete conversion. 

### Part 3: Something I Learned

In this past couple weeks, the primary takeaway that I have learned from class and from lab is how to create and use URLs and URL handlers and methods. This is not something that I had prior knowledge on or previously ever experimented with, so it was fascinating to be able to play around with URL functions and create my own to further understand how they work. 



