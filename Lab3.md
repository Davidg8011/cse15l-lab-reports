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


// chunk 3

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

* The issue was when the array had matching lowest elements. For example, {4,3,2,2} calculating the sum of this array without the lowest should be 9 but the 
* original code calculated 7. Because the code first calculates the lowest element, then when calculating the sum of the array the program does not add any element to the sum that equals the lowest. Which is fine if the lowest element is unique, but when not fine otherwise. 
