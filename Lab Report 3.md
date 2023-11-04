_**Part 1**_

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

**An input that doesn’t induce a failure, as a JUnit test and any associated code**

```
  @Test 
  public void testReverseInPlaceOneElement()
   {
    int[] input1 = {3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{3}, input1);
   }
```

**The symptom, as the output of running the tests**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/adb98286-82ce-4fce-b4f9-8150fdbebba1)


**The bug, as the before-and-after code change required to fix it**

**Before**
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
**After**
```
static void reverseInPlace(int[] arr) {
    int temp[] = new int[arr.length];
      for(int i=0; i < arr.length; i++)
      {
        temp[i]=arr[i];
      }
    for(int i = 0; i < arr.length; i += 1) 
    {
      arr[i] = temp[arr.length - i - 1];
    }
  }
```

**Briefly describe why the fix addresses the issue.**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/c6fe3b53-ab2e-43b3-b5cb-d83f6368f2d8)


The new version of the method addresses the issue because it will swap all the elements from position 0 to position n-1 of the array. While the old version of the method can only swap half elements of the array, the latter half of the array cannot be swapped. 

_**Part 2**_

**Find**

**-Exec**

`find technical/plos/ -name "*.txt" -exec wc {} \;`

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/3573c17b-8884-42df-8a35-ad5d49a0995a)

The exec command is used to execute a command on each file that matches the criteria set by the find command. In this example, the files come with number of lines, characters 

`find technical/plos/ -name "*.txt" -exec grep -l  "base pair" {} \;`

The command is used to list the names of files that contain "base pair"

**-mtime**


