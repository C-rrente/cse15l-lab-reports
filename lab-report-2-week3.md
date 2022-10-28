# Lab Report 2

[Lab Report 2](https://<C-rrente>.github.io/<your-lab-reports-repo>/lab-report-2-week-3.html)

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
	// The one bit of state on the server: a number that will be manipulated by
	// various requests.
	int num = 0;

	ArrayList<String> items = new ArrayList<String>();
	String addthis;
	String searchfor;
	public String handleRequest(URI url) {
		if (url.getPath().equals("/")) {
			return ("Welcome! Search for your item!");
		} else if (url.getPath().equals("/add")) {
			System.out.println("Path: " + url.getPath());
			String[] parameters = url.getQuery().split("=");
			addthis = parameters[1];
			items.add(addthis);
			return String.format("%s has been added!", addthis);
		} else if (url.getPath().equals("/search")){
			System.out.println("Path: " + url.getPath());
			String[] parameters = url.getQuery().split("=");
			searchfor = parameters[1];
			if(items.contains(searchfor)){
				return String.format("%s is in the list", searchfor);
			} else {
				return "That is not in the list!";
			}

		}
		return "404 Not Found!";
	}
}

class NumberServer {
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
If the user does not put a port, then main prints "Missing port number!..." Otherwise handleRequest takes the url and decides what to do with it.
In the handleRequest method I have a variable for: the word to be added, the word to search for, and the list containing the added words. 
add, within the url will add to the list, and search, within the url will search the list to see if the string is one of the elements.
Once the request is done processing, they are no longer in use, and once it is called again, these variables will be redeclared and ready to use again.


# Screenshots: 

![image](https://user-images.githubusercontent.com/71531248/198729676-7536491c-99be-4428-9430-3b3c135aa705.png)

![image](https://user-images.githubusercontent.com/71531248/198729722-3b85681d-742b-4f25-a8f2-75f41bb75f65.png)

![image](https://user-images.githubusercontent.com/71531248/198729770-f62c0811-ff69-4031-a1d4-6fd8577b5c99.png)

![image](https://user-images.githubusercontent.com/71531248/198729850-3b0e9480-b866-4eb7-9781-e5659545bba3.png)

![image](https://user-images.githubusercontent.com/71531248/198729896-e88e30f7-e387-4d7f-b97b-cebcebd6ff75.png)

![image](https://user-images.githubusercontent.com/71531248/198729914-6984869d-7e6c-4b51-bbb0-c02274a83e10.png)

![image](https://user-images.githubusercontent.com/71531248/198729934-87432401-fb4c-4e83-88fd-5140f96fad99.png)


# Part 2:

The Linked List had a failure inducing input of prepending 1 and 2.
This leads to the output of the list having one element pointing to itself.
To fix it should be that a new element is created that is used as a temp to then allow for the new element to be the new root.

The second bug is that the function averageWithoutLowest returns an integer instead of a double.
This input can be practically anything as the error is in arr.length - 1 which has nothing to do with input necessarily.
To fix, this part can be cast to a double and allow for floating point arithmetic.
