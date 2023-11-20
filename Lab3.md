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

**The Symptom**

![Image](Lab2_Add_Code_1.png) // Make this the correct .png

