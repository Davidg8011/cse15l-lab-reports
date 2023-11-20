**PART: 1**
**A Failure**
```
  @Test
  public void averageWithoutLowestTest() {
    int[] input1 = {1, 2, 3, 10, 1};
    assertEquals(4.0, ArrayExamples.averageWithoutLowest(input1), 0.000001);
  }
```

**The Symptom**

![Image](Lab2_Add_Code_1.png) // Make this the correct .png

**A test that doesn't break the code**

```
 @Test
    public void testAverageWihtoutLowest() {
      double[] input1 = {1,4,4,5};
      assertEquals(3.5, ArrayExamples.averageWithoutLowest(input1), 0.0001);
    }
```

**The Symptom**

![Image](Lab2_Add_Code_1.png) // Make this the correct .png



**The function with the bug**

```
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }

```

**The corrected method**
```
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
       sum += num; 
    }
    return (sum - lowest) / (arr.length - 1);
  }
```

*The issue was when the array had matching lowest elements. For example, {4,3,2,2} calculating the sum of this array without the lowest should be 9 but the 
*original code calculated 7. Because the code first calculates the lowest element, then the program does not add any element to the sum that equals the lowest When *calculating the sum of the array. This is fine if the lowest element is unique, but not fine otherwise. My solution to this was to calculate was to still calculate *the lowest element, once that is done simply sum up all the elements (even the lowest). Now, before calculating the average the program will remove the lowest from *the sum, Sum - lowest. This works because regardless of how many lowest elements there are one and only one is being removed from the sum, which gives us the desired behavior.

**PART: 2**
* Souce: 
[Link](https://www.geeksforgeeks.org/grep-command-in-unixlinux/#)

* grep Command

* Example: 1

* grep -c

* File:
![Image](grep_c_file.png) // Make this the correct .png

This 

*Directory:

![Image](grep_c_direct.png) // Make this the correct .png


* Example: 2

* grep -i

* File:
![Image](grep_i_file.png) // Make this the correct .png

* Directory:

![Image](grep_i_direct.png) // Make this the correct .png


* Example: 3

* grep -l

* File:
![Image](grep_l_file.png) // Make this the correct .png

* Directory:

![Image](grep_l_direct.png) // Make this the correct .png


* Example: 4

* grep -l

* File:
![Image](grep_o_file.png) // Make this the correct .png

* Directory:

![Image](grep_o_direct.png) // Make this the correct .png


