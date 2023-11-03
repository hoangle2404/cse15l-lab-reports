_Part 1_

**A failure-inducing input for the buggy program, as a JUnit test and any associated code**

```
public class ArrayTests
{
	@Test 
	public void testReverseInPlace()
  {
    int[] input1 = { 1,2,3,4,5 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 5,4,3,2,1 }, input1);
	}
```

