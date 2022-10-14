# Lab Report 2 - Server and Bugs

## Server - Search Engine
```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    List<String> list = new ArrayList<>();

    public String handleRequest(URI url) {  
        if (url.getPath().equals("/")) {
            return String.format("Current String list: %s", list.toString());
        } else if (url.getPath().contains("/add")) {
            System.out.println("Path: " + url.getPath());
            String[] parameters = url.getQuery().split("=");
            if(parameters[0].equals("s")){
                list.add(parameters[1]);
                return String.format("String added!");
            }
            return "404 Not Found!";
        } else {
            if(url.getPath().contains("/search")){
                System.out.println("Path: " + url.getPath());
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    List<String> newList = new ArrayList<>();
                    for(String str : list){
                        if(str.contains(parameters[1])){
                            newList.add(str);
                        }
                    }
                    return String.format("Words that contain " + parameters[1] + ": %s", newList.toString());
                }
                
            }
            return "404 Not Found!";
        }
    }
}
class SearchEngine {
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
## Search Engine in Action
![Image](images/server1.png)
- The ``handleRequest(URL url)`` method was called and went into the ``if (url.getPath().contains("/add))`` if statement.
- It then proceeds to split the add call by the ``=`` sign with the left side of the sign being the add type and the right side of the sign being the value added into the list

![Image](images/server2.png)
- After checking if ``parameters[0].equals("s")``, the program appends ``parameters[1]`` into the list and displays on the website that the String was added.

![Image](images/server3.png)
- Repeat of image 1 but with a different String value.

![Image](images/server4.png)
- Repeat of image 2.

![Image](images/server5.png)
- The ``handleRequest(URL url)`` method was called and went into the ``if (url.getPath().contains("/search))`` if statement.
- It then proceeds to split the add call by the ``=`` sign with the left side of the sign being the add type and the right side of the sign being the value added into the list
- After checking if ``parameters[0].equals("s")``, the program appends creates a ``newList`` and appends the relevant Strings into that list.
- It then displays that contents of that list onto the webpage.\