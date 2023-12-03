# **Lab Report 5** 

## **Part 1**

*1. The original post from a student*

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/56492b6f-4b10-4ae8-a0a7-9376d1adabfa)

Hello,
I had an issue with the `merge` method in the ListTestExamples.java when I tried to run the JUnit test. Based on the error, there must be a memory-related issue at line 42 of the ListExamples.java file. I guess the `merge` must had a hard time creating so many objects during the process of merging.

The failure-inducing input:

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/91c3828d-f2bd-4533-8974-272b4d9a5a06)

*2. A response from a TA*

Hi, 
Your guess about the error is correct. Identifying the location where the bug occurs is very important. The `merge` method might be dealing with many objects in the list or an array, and it is consuming more than the memory needed during the merge process, which will lead to the error about heap space. I recommend you have a look at the `merge` method in the ListExamples.java or use `jdb` as we learned in the class. When using jdb, try to put a breakpoint at line 43, run the program and see what the outputs are. After that, you can try to put a breakpoint at the lines above.
If you want to look at the code, try to find the reason why it consumes so much memory and try to optimize the memory problem. 

*3. Student's implementation*

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/48954815-cf17-4400-8c0c-6f2c4055b3f1)

After reviewing the `merge` method in the ListExamples file, I realized that the memory issue comes from line 43. The method used index2 to compare with the size of the list2, but incremented index1 instead of index2. This caused an infinite loop, which exceeded the memory. 

*4. Screenshots*

**The file & directory structure**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/e2250cc3-2ae7-4539-b374-4ed5aac008ec)

**The contents of each file before fixing the bug**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/4cae7a7f-034a-43c9-9808-f2001a70ccd7)


**The command to trigger the bug**

`bash test.sh`

**A description of what to edit to fix the bug**

As the output of the JUnit above, the bug is located at line 42 in the ListExamples.java file. So I changed index1 to index2 at line 43. The method used variable index2 to compare with the size of list2, but index1 is the incremented variable, so the method will run into an infinite loop because index2 is always less than the size of index2. So changing to index2 will fix the memory issue that I encountered above.   

This is the code after fixing the bug:

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/84aae47f-a494-4064-8203-32dc23502e07)

## **Part 2**

During the second half of the course, I learned a lot of new things that I did not know before. The first thing is about VIM, I would say VIM is a new experience for me. I've heard about it before but didn't have the time to practice. The second thing is writing a bash script. Finally, I learned about how to redirect output into a file using just a terminal. It is very useful for me because I won't have to make a new file and copy/paste the output by myself, so I can avoid making mistakes during the copy/paste process. 

