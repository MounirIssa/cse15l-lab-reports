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
`handleRequest(URI url)` and `public static void main(String[] args)`.
<br>
### What are the relevant arguments to those methods, and the values of any relevant fields of the class?
The argument to the handleRequest method is the URL of the page and the argument for the main method is the port number.
<br>
### How do the values of any relevant fields of the class change from this specifc request? If no values got changed, explain why?
The values of the handleRequest method change based on the user's valid query input. Every time the user puts in the correct path `/add-message` and the query `?s=[USER INPUT]`, the value of `String store` changes as it saves the user's input in the string object, store.

# Part 2:
For this part of the assignment, I have chosen the reverseInPlace method. <br>
Here is a failure-inducing input: <br>
`public void testInPlace() { 
		int[] input3 = {1, 2, 3}; 
		ArrayExamples.reverseInPlace(input3); 
		assertArrayEquals(new int[] {3, 2, 1}, input3);
	} 
` <br>
Here is the error message that pops out:
![image](https://user-images.githubusercontent.com/122484250/215299462-8f969a34-f4d7-419d-a9ad-392b2c4d13ee.png) <br>

In other words, at the second index position, we expected the value to be 1 but our program saw 3 instead. Hence, the array was not succesfully reversed. <br>

Here is a non-failure-inducing input: <br>
`public void testReverseInPlace() { 
		int[] input1 = { 3 }; 
		ArrayExamples.reverseInPlace(input1); 
		assertArrayEquals(new int[]{ 3 }, input1); 
	}` <br>
Here is the output after running the JUnit Test:
![image](https://user-images.githubusercontent.com/122484250/215299617-78ccf28c-1179-46db-abed-eeb2e1e37240.png) <br>
The green checkmerk on the left indicates a successful test. <br>

Now, to discuss why this code is not working. The symptom lies in two places: <br>
1. During the iteration, we are overwriting the values of the array from the 0th index position to the last before storing the instantaneous values somewhere. Consider the following example: <br>
Let the input array be `int[] arr = {1, 2, 3}` and let the expected output be `{3, 2, 1}`. <br>
The code in given file does the following: <br>
`{3, 2, 3} // arr[0] = arr[2]` <br>
`{3, 2, 3} // arr[1] = arr[1]` <br>
`{3, 2, 3} // arr[2] = arr[0]` <br>
Error! `arr[2] = arr[0]` is correct however we overwrote the value of `arr[0]` before storing it somewhere. To solve this dilemma, here is what we will do. <br>
1. Iterate through half the array and simultaneously replace the values of the first, with its last complement.
2. Store the values in the first half of the array before overwriting them with the last, overwrite the values of the second half with the values you stored.
<br>
Here is a demonstration: <br>
`static void reverseInPlace(int[] arr) { 
	if (arr == null || arr.length <= 1) {
		return;
	}
	for(int i = 0; i < arr.length / 2; i++) {
		int store = arr[i]; // arr[0]
		arr[i] = arr[arr.length - i - 1]; // arr[0] = arr[2]
		arr[arr.length - i - 1] = store; // arr[2] = temp (arr[0] before modification)
	}
}` <br>

Now, when we run our JUnit test, we should be good: <br>
![image](https://user-images.githubusercontent.com/122484250/215301819-ff840b4a-950a-4806-92a9-6be72e5f4b6a.png) <br>
![image](https://user-images.githubusercontent.com/122484250/215301905-b356b614-eeae-4727-ad41-c42990e47d9a.png) <br>

Success!

# Part 3:
Through this lab, I have learned the importance of debugging, writing JUnit tests, being able to understand code without having to rely on the console or terminal. I also learned how to launch web servers, something I thought Java could not do. It was very much a surprise when I saw the code for the file Server.java for the first time.






