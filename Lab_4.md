

**LAB #4**

**4) Log into ieng6**

Starting from the terminal:
 We log into the server by typing **ssh cs15lfa23tk@ieng6.ucsd.edu** and hitting <<enter>>

*5) Clone your fork of the repository from your Github account (using the SSH URL)
*6) Run the tests, demonstrating that they fail
*7) Edit the code file to fix the failing test
*8) Run the tests, demonstrating that they now succeed
*9) Commit and push the resulting change to your Github account (you can pick any commit message!)

![Image](Run_Fail_lab3.png)

```
 @Test
    public void testAverageWihtoutLowest() {
      double[] input1 = {1,4,5,6};
      assertEquals(5.0, ArrayExamples.averageWithoutLowest(input1), 0.0001);
    }
```
