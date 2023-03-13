# Lab Report 5

### Grep Command:

For the 5th and last lab report for this class, I decided to do the same exploration we did in lab report 3 for a different command. The command I've chosen is the 
grep command. Here are some of the interesting stuff I found:

1. `grep -i "STRING" file.txt`

The Grep command is, by default, case sensitive. However, slightly twisting the command by adding `-i` gets rid of the case sensitivity of the grep command. This can be very useful in case where we want to compute the total number of some item mentioned in a txt file. For data analysts who work with huge data through the terminal, this can be a life saving tool.

Here is a screenshot demonstrating how this command is used on ch1.txt within the Abernathy directory on skill-demo1-data:

![image](https://user-images.githubusercontent.com/122484250/224604251-849a08cc-77dd-4e28-adb3-bdeeb9cd625b.png)

Despite the woord "century" being written all in caps, the grep command still found what needed to be searched and returned the desired output (where the matching keywords are highlighted. This can work with any other file containing the to-be-searched keyword:

![image](https://user-images.githubusercontent.com/122484250/224604504-b13cab27-4b55-414a-a874-28c3e59062b4.png)

2. `grep -c "STRING"  file.txt`

Unlike the previous command, this one is case sensitive. It's purpose is to print the number of lines matching the given pattern (i.e. the line contains the specific word to be searched. Now, here is where magic can be done. We will combine the above command with the first, and this is what will happen:

![image](https://user-images.githubusercontent.com/122484250/224605773-446bed97-f274-43d6-b792-4d4e556902dc.png)

If you think that this is cool, wait until you see the next step. We will take this a step further and recursively print out all the number of matching lines within the txt files of a given directory:

![image](https://user-images.githubusercontent.com/122484250/224605899-336cfcb4-d1f0-4452-9c7b-339d03736c8a.png)

3. `grep -l "STRING" *`

The purpose of the `-l` part in the grep command is to print out the file names that contain the string to be searched. It can be useful when we do not want the number of lines or the lines themselves, but the file names containing those strings. This is especially true when navigating books. Here is out this command can be used:

![image](https://user-images.githubusercontent.com/122484250/224606447-48721298-85b3-408a-a59b-33f4b9dddc57.png)

`-i` instructs bash to ignore case sensitivity, and `-l` prints out not the line but the files that contain the string to be searched. Let us look at another example of how this can be used (under normal circumstances):

![image](https://user-images.githubusercontent.com/122484250/224606548-be091130-e601-43e7-a6a2-3580079ccd49.png)

4. `grep -n "STRING" file.txt`

Similar to the `-c` command, this prints out the number of lines where the to-be-searched string is found. However, this prints out the lines in a slightly different format. Further, it does not bluntly give out the number without any additional information. Here is how it is used in one scenario:

![image](https://user-images.githubusercontent.com/122484250/224607633-662e0c09-39cb-457a-a0ee-609a5deb47a6.png)

So lines 14, 35, 44, and 93 contain the string "It is". We can also take this a step further and ignore case sensitivity using the `-i` command we mentioned earlier. Here is how it can be done:

![image](https://user-images.githubusercontent.com/122484250/224607846-519e2ca5-a046-474c-b881-25bdd67362f3.png)

Suddenly it is much larger, and the number of matching lines is over 13 lines.

And this concludes my lab report 5. I had alot of fun doing this as I got to experiment combining different commands, many of which I did not add here due to me not seeing a scenario where those combinations would be used. Nonetheless, it was not boring!


Sources:
1. [OpenSource](https://opensource.com/article/21/9/linux-find-command)
2. [RedHat](https://www.redhat.com/sysadmin/linux-find-command)
3. [GeeksForGeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)


