
# CSE 15L Lab #2 Report | David Guido


![Image](Lab2_ServerCode.png)
* ServerCode


![Image](Lab2_Add_Code_1.png)

* Which methods in your code are called: HandlerRequest.

* What are the relevant arguments to those methods, and the values of any relevant fields of the class:
  The URL which is of type URI. The class has an Int and a String, the Int is to track when a string was added and the String is used to store 
  the added Strings.

* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain * why: Yes, the count gets incremented by 1 as it does with each call to HandleRequest. the string had the String "Hello" added which ultimately stores "1.  Hell\n" when the Method call is done.

![Image](Lab2_Add_Code_2.png)

* Which methods in your code are called: HandlerRequest.
  
* What are the relevant arguments to those methods, and the values of any relevant fields of the class:
  The URL which is of type URI. The class has Int and String, the Int is to track when a string was added and the String is used to store the 
  added Strings.
  
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why: Yes,
  the count will change to 2. The string will have "I hope this email finds you well" added which by the end of the method makes the string "1. 
  Hello\n2. I hope this email finds you well\n".


 In a couple of sentences, describe something you learned from lab in week 2 or 3 that you didn’t know before. 
 I learned how the split() function works. I now understand how it finds s given char and then stores everything to the left of that charr in an array at index 0 and everything to the right of the char into the same array but in index 1.
