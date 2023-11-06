# **Lab Report 3**
by Eduardo Lopez
### Part 1(Bugs with ArrayExamples from Lab 3):
Failure inducing input:
```
  @Test
  public void testingReversed1() {
    int[] original = {1,2,3,4};
    assertArrayEquals(new int[]{4,3,2,1}, ArrayExamples.reversed(original));
  }
```
Non-failure inducing input:
```
@Test
  public void testingReversed2() {
    int[] emptyArray = {};
    assertArrayEquals(new int[]{}, ArrayExamples.reversed(emptyArray));
  }
```
Symptom ouput of the two tests above:
![Image](output1.png)

The buggy method before:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
The buggy method after being fixed:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i - 1] = arr[i];
    }
    return newArray;
  }
```
The change I made was moving each element of the input array into the new array while the new array is going in reverse order. Before, it was moving the new array elements into the input array and then returning the input array. Also, I'm returning the new array as the method intended. 



