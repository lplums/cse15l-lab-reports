# Lab Report 2
## Part 1:
I created a web server called String Server using the provided code from Week 2 Lab. This code reads the path of a given
URI to find if it contains `/add-message?s=<String>` and if does, it will add this string to the running string that
with each time it is initiated, will create a new line. This will mirror a conversation.

![image](https://user-images.githubusercontent.com/122485613/215681891-1848c177-ce75-41d3-9b31-2e6af4335e10.png)

It should look like this:

![image](https://user-images.githubusercontent.com/122485613/215681981-e8f0050b-7b7e-400f-8a99-26f03d5c1166.png)

For this example, I entered the specifiied add message with the string `Hello, how are you?` in the path with ? being spaces. The method
read it, concatenated to the `String conversation`, and returned conversation in string format. The `String conversation` now holds this 
irst line for as long as this program keeps running.

![image](https://user-images.githubusercontent.com/122485613/215682042-82f77e65-becd-44b2-be46-051ccbd065a7.png)

For this example, I entered the specified add message with a different string, `Great! How about you?` in the path. Similarily, the method 
found the add message, concatenated the new string as a new line to `String converstation`, and returned this in string format. 
The `String conversation` now holds 2 lines, this line alongside the previous one.

## Part 2:
I decided to analyze the bugs in the `averageWithoutLowest` method.

This was the given method:
```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
  ```
  Here is an example where this method would be succesful:
  ```
  @Test
  public void testAverageWithoutLowest1() {
  double[] input1 = {1.0, 2.0, 3.0, 0.0);
  assertEquals(2.0, ArrayExamples.averageWithoutLowest(input1)); }
  ```
  However, here is an example where this method would fail:
  ```
  @Test
  public void testAverageWithoutLoweest2() {
  double[] input2 = {1.0, 2.0, 3.0, 2.0, 1.0};
  assertEquals(2.0, ArrayExamples.averageWithoutLowest(input2)); }
  ```
  
   It can be noted that if more than one double in the array is the same as the minimum value, then it 
   will excluded all these values in the sum which will give an incorrect averag. So therefore, it needed to be changed to 
   find the index of the minimum and only excluded that value in thee average.
   
```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    int index = 0;
    for(int i = 0; i < arr.length; i++) {
      if(arr[i] < lowest) { lowest = arr[i]; index = i;}
    }
    double sum = 0;
    for(int i = 0; i < arr.length; i++) {
      if(i != index) { sum += arr[i]; }
    }
    return sum / (arr.length - 1);
  }
  ```
  
  ## Part 3:
  During the lab on week 2 and covered in Part 1, I found it quite interesting that you can create essentially your own website on your local
  computer or a server with multiplee computers. I never knew how easy it could be to create a URL and read the path in order to manipulate
  the website.
