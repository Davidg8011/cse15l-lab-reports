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

**A Junit test that doesn't break the code**

```
 @Test
    public void testAverageWihtoutLowest() {
      double[] input1 = {1,4,4,5};
      assertEquals(3.5, ArrayExamples.averageWithoutLowest(input1), 0.0001);
    }
```
