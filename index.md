# How to log into a course-specific account?
I will summarize it into 6 steps below:
1. Access to the account. Before doing anything, you need to have an account for remote access. Go to [this website](https://sdacs.ucsd.edu/~icc/index.php). Once on the page, type in your UCSD username and PID to search for your lab account. Under the heading, additional accounts, you should be able to see a button that starts with the following
characters, cs15lwi23XX0. The last part wi23 may change depending on your quarter, click that button and proceed. There should also be a variation in the last three letters, XX0.    
![image](https://user-images.githubusercontent.com/122484250/211909679-83208c7b-8907-4e7f-ae22-3bf85738c8ed.png)
2. If this is your first time logging in, you should see a request that asks you to reset your password. Go ahead and reset your password. Write down your passowrd, and wait for 10 to 15 minutes. The page should have the head title, global password reset.  
![image](https://user-images.githubusercontent.com/122484250/211909856-d95b3394-f469-4174-9871-fbae072a3472.png) 
3. Open VSCode, if you do not have it installed, go to [this website](https://code.visualstudio.com/) and download it. Setting things up should be pretty simple, not much to do. I already had VSCode and I am assuming you do too since CSE 11 and/or 8B, classes that use Java, are prerequisites for this course.
5. Next, go to VSCode, open a new terminal on VSCode and type the following: <br>
`$ ssh cs15lwi23XX0@ieng6.ucsd.edu`
Replace XX0 with your own account's letters.
5. You will receive a confirmation request asking you whether you really want to continue, type yes and continue.
6. Upon success, you will see this on your screen:  
![image](https://user-images.githubusercontent.com/122484250/211909019-143e22c9-95e7-49db-a7c9-868ff4f94b03.png)

Trying some git commands:
1. Logging into the remote server, yours may look a little different if it is your first time doing this:
`ssh cs15lwi23XX0@ieng6.ucsd.edu`
After typing my password, the process was successful
![image](https://user-images.githubusercontent.com/122484250/214968261-9f35df53-282d-4bdb-b1ae-b53f4ce5685b.png)
2. Checking current directory:
`pwd`
![image](https://user-images.githubusercontent.com/122484250/214968450-dac427b1-c006-4204-a987-141411225f09.png)
This shows which directory you are currently in. To get out of a directory, use the command `cd ..` and to go into a path, use the command `cd fileName`.
3. Checking the files in your directory:
`ls`
![image](https://user-images.githubusercontent.com/122484250/214968723-3e4b46e4-ca42-4203-bb13-acd8aedde73e.png)
And by doing `cd newFile`, try guessing what my current directory is before you look at the image below.
Bingo!
![image](https://user-images.githubusercontent.com/122484250/214968860-451b0d46-0cca-475c-9a24-ae278e9c3965.png)

There are many more commands for you to try such as `mkdir fileName` to create a new empty directory, or scp to copy and/or update files from your local computer
to thr remote server.


I had some experience working with the terminal when doing this because I have been doing some web development work. This is why things may feel fast-paced however manipulating directory paths and using git commands is way simpler than you think. My advice is to just go for whatever idea you have in mind; surf the internet, look up commands, and do whatever interests you. The worst that could happen is an error, there is no harm in trying at all. After all, we learn through failure!
