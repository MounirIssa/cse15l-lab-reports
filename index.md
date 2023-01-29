# Lab Report Two:

## Part 1:
### Code Screenshot(s):
![image](https://user-images.githubusercontent.com/122484250/215291495-9bee598b-05a7-41a2-b600-527d8e324a7f.png) <br>
<br>
![image](https://user-images.githubusercontent.com/122484250/215292080-ebb0dbe1-e652-47bc-bf2b-15c04764f4f7.png) <br>

### Output Screenshot(s):
![image](https://user-images.githubusercontent.com/122484250/215298866-3862e4ad-89aa-4714-a307-d74a4011dbaf.png) <br>
<br>
![image](https://user-images.githubusercontent.com/122484250/215298885-5c031769-6622-4079-aa61-560c3324a190.png) <br>
<br>
### Which methods in your code are called?
The class StringServer, implemented the interface URLHandler. Inside the class, I overrode the method handleRequest, whereby I implemented the desired functionality of my server. Upon calling the class StringServer() in the main method, - the method responsible for taking in the port number and initiating the web server on my local server - the handleRequest method was called to give my url it's desired functionality.
In conclusion, the two methods called are the handleRequest method that takes in a URL, and the main method, that takes in the port number.
<br>
### What are the relevant arguments to those methods, and the values of any relevant fields of the class?
The argument to the handleRequest method is the URL and the argument for the main method is the port number.
<br>
### How do the values of any relevant fields of the class change from this specifc request? If no values got changed, explain why?
The values of the handleRequest method change based on the user's valid query input. Every time the user puts in the path `/add-message` and the query `?s=[USER INPUT]`, the value of `String store` changes as it saves the user input in a string object.

# Part 2:
For this part of the assignment, I have chosen the reverseInPlace method.
Here is a failure-inducing input:
`public void testInPlace() {
		int[] input3 = {1, 2, 3};
		ArrayExamples.reverseInPlace(input3);
		assertArrayEquals(new int[] {3, 2, 1}, input3);
	}
` <br>
Here is the error message that pops out:
![image](https://user-images.githubusercontent.com/122484250/215299462-8f969a34-f4d7-419d-a9ad-392b2c4d13ee.png) <br>

In other words, at the second index position, we expected the value to be 1 but our program saw 3 instead. Hence, the array was not succesfully reversed. <br>

Here is a non-failure-inducing input:
`public void testReverseInPlace() {
		int[] input1 = { 3 };
		ArrayExamples.reverseInPlace(input1);
		assertArrayEquals(new int[]{ 3 }, input1);
	}` <br>
Here is the output after running the JUnit Test:
![image](https://user-images.githubusercontent.com/122484250/215299617-78ccf28c-1179-46db-abed-eeb2e1e37240.png) <br>
The green checkmerk on the left indicates a successful test. <br>

Now, to discuss why this code is not working. The symptom lies in two places: <br>




