# How to log into a course-specific account?
I will summarize it into 7 steps below:
1. Access to the account. Before doing anything, you need to have an account for remote access. Go to https://sdacs.ucsd.edu/~icc/index.php. Once on the page, type
in your UCSD username and PID to search for your lab account. Under the heading, additional accounts, you should be able to see a button that starts with the following
characters, cs15lwi23ABC. The last part wi23 may change depending on your quarter, click that button and proceed. There should also be a variation in the last three letters, ABC.    
![image](https://user-images.githubusercontent.com/122484250/211909679-83208c7b-8907-4e7f-ae22-3bf85738c8ed.png)
2. If this is your first time logging in, you should see a request that asks you to reset your password. Go ahead and reset your password, remember it, and wait for
10 to 15 minutes. The page should have the head title, global reset password.  
![image](https://user-images.githubusercontent.com/122484250/211909856-d95b3394-f469-4174-9871-fbae072a3472.png) 
3. Open VSCode, if you do not have it installed, go to https://code.visualstudio.com/ and download it. Setting things up should be pretty simple, not much to do. I
already had VSCode and I am assuming you do since CSE 11 and 8B, classes that use Java, are a prerequisite for this course.
5. Next, go to VSCode, open a new terminal on VSCode and type the following:
$ ssh cs15lwi23ABC@ieng6.ucsd.edu
Replace ABC with your own account's letters.
5. You will receive a confirmation request asking you whether you really want to continue, type yes and continue.
6. Upon success, you will see this on your screen:  
![image](https://user-images.githubusercontent.com/122484250/211909019-143e22c9-95e7-49db-a7c9-868ff4f94b03.png)
7. Try some git commands and have fun!!

I had some experience working with the terminal when doing this because I have been doing some wed development work. This is why things may feel fast-paced however manipulating directory paths and using git commands is way simpler than you think it is. My advice is to just go for whatever idea you have in mind; surf the internet, look up commands,
and do whatever you can find. The worst that could happen is an error, there is no harm in trying at all. After all, we learn through failure!
