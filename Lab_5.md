
**LAB #5 David Guido**


1) The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is. (Don’t actually make the post! Just write the content that would go in such a post)

**Student Post**

* Hello, 
*
* I am having trouble debugging my code. The code can run from the terminal when I type "Javac Main.java"
* followed by java Main 15. However, I cannot get the code to run from a bash script file.
* This makes me think the issue must be with the bash file.

![Image](Lab_4_log_Into_ieng6.png)





2) A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)


**TA Response**

* Hello,

* Looks like you're most of the way there! just a few issues left, I noticed that the total number of primes seems to be off by 1 can you send me a screenshot of your method that calculates if a number is prime or not? Going back to your bash script it seems the way you're handling the input seems to be funky. Remember that values passed into bash are accessed using $1, $2 etc. So you .sh file should have a line that reads "Java Main $1" 

Lmk if that helps any!



3) Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.


4) At the end, all the information needed about the setup including:
a) The file & directory structure needed
b) The contents of each file before fixing the bug
c) The full command line (or lines) you ran to trigger the bug
d) A description of what to edit to fix the bug
  
![Image](Lab_4_log_Into_ieng6.png)

