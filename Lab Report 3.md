_**Part 1**_
-----------------

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
---------------

# Find

## -exec

Source: https://www.computerhope.com/unix/ufind.htm

`find technical/plos/ -name "*.txt" -exec wc {} \;`

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/3573c17b-8884-42df-8a35-ad5d49a0995a)

The exec command is used to execute a command on each file that matches the criteria set by the find command. In this example, the files come with number of lines, characters 

`find technical/plos/ -name "*.txt" -exec grep -l  "base pair" {} \;`

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/1576b002-03e7-4326-bade-306a0f7ef316)


The command is used to list the names of files that contain "base pair"

## -mtime

Source: https://www.computerhope.com/unix/ufind.htm

`find technical/plos -name "*.txt" -mtime  +20`

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/79c4c4d0-3a07-4409-8594-5e1d18ffe52e)

The command allows me to find files that were modified 20 days ago.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/18dd2a05-b19d-4fea-8aaf-2687140fb817)

`find technical/plos -name "*.txt" -mtime  0`

The command allows me to find text files that were modified within the last 24 hours.

## -empty
Source: https://www.computerhope.com/unix/ufind.htm

`find technical/plos -name "*.txt" -empty`

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/2451811a-e3d0-4e6f-ac8d-fa345fcd1a92)

The empty flag allows me to find empty text files in /technical/plos

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/bb26545f-c07d-4893-8659-ffc53138e2a0)

`find technical/biomed -name "*.txt" -empty`

The command allows me to find empty text files in /technical/biomed

## -readable

Source: https://www.computerhope.com/unix/ufind.htm

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/423ab595-aef2-456c-a665-a2907ef04227)

`find technical/biomed -name "*.txt" -readable`

The command allows me to find every text file that is readable in technical/biomed

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/08b77c48-e295-43ab-a170-58800e70b47b)

`find technical/plos -name "*.txt" -readable`

The command allows me to find text files that readable in technical/plos. 
