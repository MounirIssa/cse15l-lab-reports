# Lab Report 3

### Find Command:

Here are some of the new commands I found:

* `find . -type "TYPE" -empty`

This command works like the normal find, however there's a slight twist. First, the keyword `-type` tells the find command that we are searching for something even
more specific, a directory (d), file (f), symbolic link (l), etc.... This helps limit the broadness of our search, especially in an environment with huge chunks of data spread all over the place. The keyword `-empty` provides further specificity and tells the command to look for empty directories, files, etc... This can be very useful in cases where we want to clean up our server.

Here is a screenshot that demonstrates the usage of this command:


![image](https://user-images.githubusercontent.com/122484250/218277116-f5dfd2f0-97b3-4227-8272-6edf81aace41.png)

The reason this is empty is because there are no files within the directory `written_2` (or its subdirectories) that are empty.

![image](https://user-images.githubusercontent.com/122484250/221761646-93ac6b06-6831-42cc-beab-4e45986c2a6a.png)

This is another example that showcases the usage of the above command; this time, we are searching for empty directories. 



* `find <directory> -ls`

This command lists the contents of a directory recursively, meaning that it doesn't just list the target you provide for it, but also descends into every subdirectory within that target (and every subdirectory in each subdirectory, and so on.), printing all paths. This can be useful in cases where we want to print out all the
content of a directory, and observe what changes could be made to better organize the data.

![image](https://user-images.githubusercontent.com/122484250/221762780-eff68df1-e554-49aa-b19d-4aa46b227565.png)

The list for this specific example goes on and on. 

Here is another example that is rather more specific and concise:

![image](https://user-images.githubusercontent.com/122484250/221763080-8fa7193a-cf68-46fc-82fd-4ccdf0a5bef5.png)

This prints all the content inside the directory Berk recursively.


* `find . -maxdepth "DEPTH"`

With hundreds of files in a default user directory and thousands more outside of that, sometimes you get more results from find than you want. This command helps
you limit the depth of your searches with the keyword `-maxdepth`.

Here is an instance where this command is used:

![image](https://user-images.githubusercontent.com/122484250/218277364-2e3eb4c4-6286-4649-8dcc-a84927eb66e9.png)

In this scenario, `./written_2` is considered as the main directory, and `-maxdepth 2` means that the depth of the tree we want to search inside this folder, is 2. This means the find command will only search the files that are directly residing inside the main directory, and the files residing within them. It is not a recursive function like `find .` that prints out every folder/file within the subdirectories. Rather, it knows where to stop based on the input arguments.

This is another example showcasing the command's usage:

![image](https://user-images.githubusercontent.com/122484250/221763740-78faf734-c2b2-41f3-bed2-0bce35c23a7d.png)


* `find . -mindepth "DEPTH"`

As you can guess, if `-maxdepth` is used to control how deep into our folders we want `find` to descend to, `-mindepth` is the exact opposite, it is used to set the minimum depth of recursion. In simple words, `-maxdepth` is the maximum depth of recursion whereas `-mindepth` is the minimum. This can also be very helpful when working with really large files. Therefore, the usage of both these keywords really depends on our needs and the environment we're working in.

Here is a screenshot displaying this command in use:

![image](https://user-images.githubusercontent.com/122484250/218278261-767a2c17-0520-4f3a-8db8-dfeff3f12476.png)

Here is another example using `-mindepth`:

![image](https://user-images.githubusercontent.com/122484250/221764093-53cb403c-82f2-4158-9c59-dfd517fb9fc2.png)


And this concludes my lab report 3, hope you found it useful!!

Sources:
1. [OpenSource](https://opensource.com/article/21/9/linux-find-command)
2. [RedHat](https://www.redhat.com/sysadmin/linux-find-command)


