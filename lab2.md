PART 1:

Here's the code for my StringServer.

![Image](code1.png)

When I call upon </add-message?s=Hello>, you can see below that the message, Hello appears. Firstly, the code initializes the variable message, which is empty
right now since this is the first time we're adding a message. Then the if statemate checking to see if our request has /add-message in it runs, and since we do have
that, we initialize string query to get the query of our url. Then an if statement runs to make sure the query isn't empty and that the query starts with s=. Since
we have those, we initialize String newMessage with that of the text after s=. Then we concatenate message with newMessage to add upon the existing message passing
the if statement to check if the message was blank. With this code being, run, the website should finally display our message, Hello. 

![Image](pic1.png)

As for calling upon a second add message, this time with </add-message?s=How are you>. The code will run identically to what I described above. However, remember that 
our message from last time will save. So message will initalize with value "Hello". However this time the if statement where it checks if message is blank will be put
into play here now. Since our message is not blank now, our new message will now be consisting of the original message and then a new line with the new message we put.

![Image](pic3.png)

PART 2

For reverseInPlace, this JUnit test makes the code fail. 

![Image](code4.png)

Here's the code that will fix it.

```
static void reverseInPlace(int[] arr) {
   int newArr[] = new int[arr.length];
   for(int i = 0; i < arr.length; i += 1) {
     newArr[i] = arr[arr.length - i - 1];
   }
   for (int i = 0; i < arr.length; i++) {
    arr[i] = newArr[i]
   }
 }
 ```
 This would fix the code because the previous code failed to take into account the elements shifting during the for loop, messing with the reverse operation.
 By creating a new array, this would avoid the shift in elements. Then you just simply copy the new array onto the old one.
 
 PART 3
 
 One thing I learned in week 2 was learning how to start up my own remote server and accessing it through local host. I didn't know at all how to even start up
 a server and I didn't know you could access that server from my very own website. Learning how to do that using VSCode was quite the learning experience.
 
 
