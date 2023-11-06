**The buggy Function**
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

**The Junit test which breaks the code**

```
 @Test
    public void testAverageWihtoutLowest() {
      double[] input1 = {1,1,4,4,5};
      assertEquals(3.5, ArrayExamples.averageWithoutLowest(input1), 0.0001);
    }
```

**A Junit test that doesn't break the code**

```
 @Test
    public void testAverageWihtoutLowest() {
      double[] input1 = {1,4,4,5};
      assertEquals(3.5, ArrayExamples.averageWithoutLowest(input1), 0.0001);
    }
```
