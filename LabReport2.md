# Part 1
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/b3c16f44-5f31-483d-9e0d-5d9f5b3368c8)

2. 
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/6fce9765-5576-473d-9501-458eee01f6d1)
The methods that are being called are the handleRequest() method in the Handler class and the start() method in the Server.java file to create the server. The relavent arguments to the handleRequest() method is the URI url. Initially, the value of URI url is [http://localhost:4000/](http://localhost:4000/); ArrayList inputs is a blank ArrayList; and String result has a blank string. After the request, the URI url gets repopulated with [http://localhost:4000/add-message?s=Hello](http://localhost:4000/add-message?s=Hello), array String[] parameters gets populated with 2 values, the url http://localhost:4000/add-message?s as a String and the String inputted after /add-message?s= (in this case "Hello"). The fields that change afterwards is the ArrayList inputs, which adds the String "Hello", and the String result, and since there was only one input, it would be "1. Hello\n".

3. 
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/e70d9fd0-f145-421a-bb9b-6626a057b89a)
The methods that are being called are the handleRequest() method in the Handler class. The relavent arguments to the handleRequest() method is the URI url. Initially, the value of the URI url is [http://localhost:4000/add-message?s=Hello](http://localhost:4000/add-message?s=Hello); ArrayList inputs is an ArrayList with only one value, "Hello" at index 0; and String result would be already populated with "1. Hello\n". After the request, the URI url gets repopulated with [http://localhost:4000/add-message?s=How are you](http://localhost:4000/add-message?s=How are you) and array String[] parameters gets populated with 2 values, the url http://localhost:4000/add-message?s, and the String inputted after /add-message?s= (in this case "How are you"). The fields that change after this request is the ArrayList inputs, which adds the String "How are you" (this makes the size of the ArrayList 2), and the String result, and since there are now 2 inputs, it would be "1. Hello\n2. How are you\n".

# Part 2
