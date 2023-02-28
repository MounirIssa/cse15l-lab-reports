# Lab Report 4

**1. Log into ieng6**:

*Keys Pressed:* `<Ctrl+R> <ssh> <enter>`

Because I have logged into ieng6 several times on my computer, reverse history lets me look up all instances where ssh was used. Thus, upon clicking the keys Ctrl+R, I 
typed in ssh, and my account popped up so all I had to do was hit enter. This saves me alot of time and prevents potential errors that may arise due to typos.

![image](https://user-images.githubusercontent.com/122484250/221734327-eac030a9-74a3-47f9-a704-9555af42e3d9.png)

**2. Clone fork of the repository from Github account**

*Keys Pressed:* `<git clone url> <Ctrl+C> <Ctrl+V>`

Not much was done in this step; all I did was clone the url of the forked repository using a git command, namely the git clone command. I copied the link normally 
using <Ctrl+C> and pasted the link using Ctrl+V.

![image](https://user-images.githubusercontent.com/122484250/221735654-1a30e179-55f7-4884-b427-354d72e66efe.png)

**3. Run the tests; demonstrate their failure**

*Keys Pressed:* `<Ctrl+C> <Ctrl+V>`

I do not have the compile and run commands saved so I had to copy and paste it from the course webpage, ![here](https://ucsd-cse15l-w23.github.io/week/week3/).

![image](https://user-images.githubusercontent.com/122484250/221737007-d15e3065-40ce-4e90-878e-61d1169cb4a6.png)

**4. Edit the code file to fix the failing test**

*Keys Pressed:* `<nano filename>` `<down, left, right>` `<Ctrl+O>` `<enter>` `<Ctrl+X>`

To edit the file and fix the error, I used the command `nano ListExamples.java`. I used the up, down, left, amd right keys to navigate my way through the file. I found
the error lying around line 43, fixed it, clicked the keys Ctrl+O, enter to save, and Ctrl+X to quit. 

![image](https://user-images.githubusercontent.com/122484250/221740454-958b624f-40e8-49c7-b28a-fb9d8ac704ab.png)

**5. Run the tests, demonstrating that they now succeed**

*Keys Pressed:* `<up><up><up><enter>` `<up><up><up><up><enter>`

The `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was 3 up in the search history, so I used up arrow to access it.
Then the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore` command was 4 up in the history, so I accessed and ran it in
the same way.

![image](https://user-images.githubusercontent.com/122484250/221741367-ea27de82-ecd7-4177-9813-1f4182a25c6d.png)

**6. Commit and push the resulting change to your Github account**

*Keys Pressed:* `<git add .>` `<git commit -m "Updated File">` `<git push>`

After changing the contents of ListExamples.java, I committed and pushed the changes I made to my github account. And the below image was the resulting output.

![image](https://user-images.githubusercontent.com/122484250/221746970-fb3cb882-af95-4950-9108-b4043ecbdf3b.png)


