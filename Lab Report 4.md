**Lab Report 4**

*Step 4*

Key pressed: `ssh cs15lfa23lo@ieng6.ucsd.edu`

I logged into ieng6 using the `ssh` command.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/c55b9800-e14b-4c80-8289-186bd750c16e)


*Step 5*

Key pressed: `git clone git@github.com:hoangle2404/lab7.git` `<Enter>`

First I logged into the ieng6 account, then `git clone` the repository from my GitHub account

The git clone command cloned the SSH URL.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/089dca3f-7165-4b8f-972c-f04d13f3c9c4)

*Step 6*

Key pressed: `bash test.sh` `<Enter>`

After cloning the repository, I changed the working directory to lab7 by using `cd lab7`
Then run `bash test.sh`

The command runs the test.sh file to run the tests.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/327e7490-8e88-4fb7-9756-86345acdb308)

*Step 7*

Key pressed: `:44s/1/2` `<Enter>`  , `vim ListExamples.java` `<Enter>`

I then used `vim ListExamples.java` `<Enter>` to access the file. 
After that I press `:44s/1/2` to change the parameter from index1 to index2

The command located line 44 and then substituted the number 2 for 1.
44: the line number where the substitution command is applied. s: substitute. /1: the pattern to be replaced. /2 the replacement pattern.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/6d847690-c188-4ce1-ae22-424c00f8a8a2)


Key pressed: `:wq` `<Enter>`

After finished editing the file, I saved and quit the file using `:wq` `<Enter>`

The command will save and then quit the file. 
'w': save the changes made to the file
'q': quit the file

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/b8737e17-1eab-4278-b726-8b3947ebfbca)


*Step 8*

Key pressed: `<up><up>` `<Enter>`
The `bash test.sh` command was 2 up in the search history, so I pressed the up arrow 2 times to access it. 

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/d325a92e-f6c3-4e6d-9f1e-268cf534a61a)

*Step 9*

Key pressed: `git add ListExamples.java` `<Enter>`  

The `git add` command will add changes to staging area and make sure that ListExamples.java will be ready to be committed.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/78fae7ef-e0e1-4f8a-aa4d-06b596827920)


Key pressed: `git commit` `<Enter>` , `index1 -> index2` `<Esc>` , `:wq` `<Enter>`

I used `git commit` command, and then a message appeared, asking me about the commit message for the change. After entering the message, I used `:wq` to save and quit. 

The `git commit` allows you to save changes made to the files in the repository. A test editor will appear when we run `git commit`, which allows us to enter the commit messages to describe the changes.

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/9235572d-dfae-40e4-b0da-e17a79e92600)

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/fe6be588-654b-4fd1-a943-4ec9e7d7f972)

Key pressed: `git push` `<Enter>`

The `git push` command is used to send the committed changes when using `git commit` from the local repository to a remote repository. 

![image](https://github.com/hoangle2404/cse15l-lab-reports/assets/146885173/274abf29-efa3-4075-99ef-3c8f4b65f558)

