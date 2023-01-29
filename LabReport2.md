## Part 1

## Part 2

A failure inducing test:
```
@Test 
	public void testReverseInPlace() {
    int[] input2 = {2,4,6,5,8};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{8,5,6,4,2}, input2);
	}
```
A passing test:
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
Failing test screenshot
<img src = "/LabReport2/TestingB4Fail.png" weight = "20%" height = "20%"/>
Passing test screenshot 
<img src = "/LabReport2/TestingB4Pass.png" weight = "20%" height = "20%"/>
## Part 3
