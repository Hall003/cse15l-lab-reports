## Part 1

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> strings = new ArrayList<String>();
    public String handleRequest(URI url) {
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            strings.add(parameters[1]);
            return String.join("\n", strings);
        }
        return "Hi!";
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

## Part 2

A failure inducing test:
```
@Test 
	public void testReverseInPlace() {
    int[] input2 = {2,4,6,5,8};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{8,5,6,4,2}, input2);
	}
```
A passing test:
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
Failing test screenshot:
<br/>
<img src = "/LabReport2/TestingB4Fail.png" width = "50%" height = "50%"/>
<br/>
Passing test screenshot: 
<br/>
<img src = "/LabReport2/TestingB4Pass.png" width = "50%" height = "50%"/>
<br/>
Code before:
<br/>
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  ```
  <br/>
  Code After:
  <br/>
  
  ```
  static void reverseInPlace(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    for (int i = 0; i < arr.length; i ++){
      arr[i] = newArray[i];
    }
  }
  ```
  
  <br/>
  
 The original code attempted to switch the elements around, but once it reached the middle it just copied the first half again. The after code created a new array and populated the new array with the flipped array. It is then copied over into the original array.
## Part 3
I didn't realize you could create a web server so easily and have things change based on what's typed into the search bar. I guess I knew it was a possibility, but I had never looked into it enough to understand how it worked. To be honest I still don't completely understand how it works, although I'm sure I can figure it out after testing things out for a while more.
