# Lab Report 2

##  Servers and Bugs

### Part 1:

For tis lab, I created a StringServer class that suppports the path and behavior of keeping track of a single string that gets added to by incoming requests. Here is my code for the method that does this:

![Code.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Code.png)

I then launched the localhost and played around with the possible requests. For the screenshots below, the handRequest method (for which I poseted the code above) is what is called. The add-message value is given at the end of the URL, which allows the query to follow. The complete request then looks like `/add-message?s=` followed by the String to be added. In the latter screenshots, you can then see how the next String requests are added to the existing String to be displayed on a new line each time.

![Message1.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Message1.png)

![Message2.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Message2.png)

![Message3.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/Message3.png)

Lastly, I tried to make an `/add-message?` request without properly adding the `s=` query format, which resulted in an error message as it was supposed to. 

![NotFound.png](https://raw.githubusercontent.com/advikasonti/cse15l-lab-reports/main/NotFound.png)

### Part 2:



