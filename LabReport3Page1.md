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


