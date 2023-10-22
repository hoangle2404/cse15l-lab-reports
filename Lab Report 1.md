# Lab Report 1

## cat
**Using the command with no arguments:**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/dc808caa-da09-4519-b97f-410768e7b6c9)

* The working directory is: /home
* No argument means there are no files, or paths given.
* For the output, when running cat command without any arguments, nothing happens. When I input something later, the output is exactly what the input is.   
* Having no argument means you don't put anything in the command, directory, or path.
* This is not an error. It's not an error because this is an expected behavior of the command. Since we did not pass any path for it, it will read the input. The execution of the command will never stop unless I use ctrl + c.     

**Using the command with a path to a directory as an argument**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/4b7ab277-45bc-410a-b0a6-a0440499227e)

* The working directory for this one is /home/lecture1
* For the output, when running cat with a path to a directory as an argument, the output will print "/home/lecture1 is a directory". The cat command prints the content of the file(s), and the path I gave it was a path to the directory. So, instead of printing the content of the file, it shows that "/home/lecture1" is a directory. 
* This is an error. The cat command is used to read the content of files. So it cannot print out the contents of a directory like it does for a file. 

**Using the command with a path to a file as an argument**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/9f1a3f8a-9a40-4dd7-9b33-619eaece20ad)

* The working directory is /home/lecture1/messages
* For the output, the cat command will print "Hello World!". The cat command prints the content of the file(s), and since I put the path to the en-us.txt file, it will print the content of the file, which is Hello World!
* This is not an error. 

## ls
**Using the command with no arguments:**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/d01dba85-b9a1-431c-a26e-eb6af261bb26)

* The working directory is: /home
* For the output, the ls command lists all the files or folders in the path. Having no argument means you don't put anything in the command, directory, or path. Since there was no argument in the path, it will print all the folders in the working directory.
* This is not an error.

**Using the command with a path to a directory as an argument**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/23abea2a-4dde-40f1-a494-8de384a5469c)

* Working directory: /home/lecture1
* For the output, I used ls /home/lecture1. All the files and folders in the system were: Hello.java  messages  README  URIMain.class. So ls will list all the files and folders in the path, which will print all the files and folders above.
* This is not a bug.

**Using the command with a path to a file as an argument**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/1ff4276e-8c8c-4653-be48-cfdfe8c63183)

* The working directory: /home/lecture1/messages
* For the output, the ls command is used to list all the files and folders. If we give it a specific file, it will print the path to the file instead of the content because there are no files or folders in the file. 
* This is not a bug.

## cd

**Using the command with no arguments:**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/e383ce77-2227-42f8-8508-11e3431bfb6b)

* Working directory: /home
* For the output: At first, my directory was lecture1, and after I used cd, the directory changed to /home. Because I did not put any argument to the command, it will automatically understand that I want to change to /home.
* This is not a bug.

**Using the command with a path to a directory as an argument**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/d5669727-f4b7-403e-93e8-a7be7654dd18)

* Working directory: /home/lecture1/messages
* For the output: When I put a path to the directory as an argument, the program changed the directory from /home to /home/lecture1/messages as we can see in the screenshot.
* This is not a bug.

**Using the command with a path to a file as an argument**

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/5dc90c42-09fb-434f-816f-4a74be143805)

* Working directory: /home/lecture1/messages
* For the output: Since cd is used to switch the directory, and the given path is the path to a file, cd cannot switch the directory to a file because we cannot use a file as the directory.
* This is not a bug. 





