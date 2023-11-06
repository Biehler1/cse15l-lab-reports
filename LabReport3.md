# Lab 3
## Part 1
Bug: The bug that we are going to examine is the reversed() method from the ArrayExamples.java class. The problem seems to be that the original reversed() method would change the inputted array, and assign it blank (0) values from a new array that was created. Therefore, the fix seems to be just to switch the new array with the old array in the code and return the new array.

1. Failure Inducing Input: 
```
  @Test
  public void testReversed3Inputs() {
    int[] input = {1, 2, 3};
    int[] temp = {1, 2, 3};

    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input));

    //Checks that the original array wasn't changed
    assertArrayEquals(temp, input);
  }
```
2. Non-Failure Inducing Input:
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
3. Symptom:
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/45a83193-a815-4fa2-a871-9b73f33ca9cc)
4. Bug fix:

Before:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; ++i) {
      newArray[arr.length-1-i] = arr[i];
    }
    return newArray;
  }
```

Explanation:
Originally, the issue was that the original array (arr) was assigned values from the new array created (newArray that had all 0 values) instead of the other way around. Then, it returned the original array (arr) when it was supposed to return a new array (newArray). To fix this, I flipped the assignment of values from the new array (newArray) to the old array (arr) to the assignment of values from the old array (arr) to the new array (newArray). This was demonstrated through changing the line `arr[i] = newArray[arr.length - i - 1];` to `newArray[arr.length-1-i] = arr[i];`. To make sure the program returned a new array instead of changing a pre-existing one, I also made sure to make the program `return newArray;` instead of `return arr;`. These changes made it so the reversed() method worked properly and that the values of the original array (arr) wasn't changed at all, just like the description of the method.
