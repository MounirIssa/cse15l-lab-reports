# Lab Report 3

### Find Command:

Here are some of the new commands I found:

1. `find . -type "TYPE" -empty`

Here is a screenshot that demonstrates the usage of this command:


![image](https://user-images.githubusercontent.com/122484250/218277116-f5dfd2f0-97b3-4227-8272-6edf81aace41.png)

The keyword `-type f` tells it that the files to be searched are files. And `-empty` tells it to search for the empty directories inside written_2. The result is empty
because there are no empty files inside written_2.

2. `find . -empty`

Here is a screenshot that displays the output:

![image](https://user-images.githubusercontent.com/122484250/218277068-9176908a-98f3-4883-a010-1cf438e42213.png)

The reason this list is longer is because the find command searches for all empty files, directories, etc... inside the skill-demo1-data. It does not differentiate between txt files and directories/paths.

3. `find . -maxdepth "DEPTH"`

Here is a screenshot of an output:

![image](https://user-images.githubusercontent.com/122484250/218277364-2e3eb4c4-6286-4649-8dcc-a84927eb66e9.png)

In this scenario, `./written_2` is considered as the main directory, and `-maxdepth 2` means that the depth of the tree we want to search inside this folder, is 2. This means the find command will only search the files that are directly residing inside the main directory, and the files residing within them. It is not a recursive function like `find .` that prints out every folder/file within the subdirectories.

4. `find . -mindepth "DEPTH"`

Here is a screenshot displaying this command in use:

![image](https://user-images.githubusercontent.com/122484250/218278261-767a2c17-0520-4f3a-8db8-dfeff3f12476.png)

As you can guess, if `-maxdepth` is used to control how deep into our folders we want `find` to descend to, `-mindepth` is the exact opposite, it is used to set the minimum depth of recursion. To put it in simple words, `-maxdepth` is the maximum depth of recursion, `-mindepth` is the minimum. This can be very helpful when working with really large files.

### Grep Command:

1. `grep -i "STRING" file.txt`

Here is an image showing how this is used:

![image](https://user-images.githubusercontent.com/122484250/218278622-b7957d60-84b5-481f-99b7-f389ddc9c3ca.png)

The keyword `-i` ignores case and only searches for strings inside the given file that matches what the user put. Now, this is not very useful on it's own but you will see how it will come to use in the following command.

2. `grep -c "STRING" file.txt`

Here is an image:

![image](https://user-images.githubusercontent.com/122484250/218278685-a046336b-d592-427a-a9cd-ff1c320b56d3.png)

This command prints a count of the lines that mactch the given pattern; unlike the previous one however, this command is case sensitive thus accuracy is extremely important.

3. `grep -l "STRING" *`

Here is how this command can be used:

![image](https://user-images.githubusercontent.com/122484250/218278797-3beae997-15cc-48cc-b090-26a08be8e2d6.png)

The purpose of the `-l` part of this command is to display a list of file names with the string to be searched. In other words, disregarding case sensitivity, all these files have the strinng "History" in them.

4. `grep -n "STRING" file.txt`

Here is an output:

![image](https://user-images.githubusercontent.com/122484250/218278868-0da19d68-6e6b-46cb-aced-87917bbe1ea3.png)

The purpose of this command is similar to `grep -i`. The difference however is that this command prints out the line number inside the file where matching strings were found. This can be very helpful for data analysts who may use the terminal or linux in general.


This concludes my research for lab report 3, I do want to say though, that I indeed learned alot from this. Despite passing the skill demonstration, I would have had a much easier time preparing for it if I had done the lab report earlier.


Sources:
1. [GeeksforGeeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
2. [OpenSource](https://opensource.com/article/21/9/linux-find-command)
3. [RedHat](https://www.redhat.com/sysadmin/linux-find-command)


