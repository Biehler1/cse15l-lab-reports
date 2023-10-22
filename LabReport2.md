# Part 1
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/b3c16f44-5f31-483d-9e0d-5d9f5b3368c8)

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/caa37e1e-1eda-4e02-ab80-f24a1e8323f1)
2. The methods that are being called are the handleRequest() method in the Handler class and the start() method in the Server.java file to create the server. The relavent arguments to the handleRequest() method is the URI url. Initially, the value of the ArrayList inputs is a blank ArrayList, String result has a blank string, and the array String[] parameters gets populated with 2 values, the url, and the String inputted after /add-message?s= (in this case "Hello"). The fields that change after this request is the ArrayList inputs, which adds the String "Hello", and the String result, and since there was only one input, it would be "1. Hello\n".

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/e70d9fd0-f145-421a-bb9b-6626a057b89a)
3. The methods that are being called are the handleRequest() method in the Handler class. The relavent arguments to the handleRequest() method is the URI url. Initially, the value of the ArrayList inputs is an ArrayList with only one value, "Hello" at index 0, String result would be already populated with "1. Hello\n", and the array String[] parameters gets populated with 2 values, the url, and the String inputted after /add-message?s= (in this case "How are you"). The fields that change after this request is the ArrayList inputs, which adds the String "How are you" (this makes the size of the ArrayList 2), and the String result, and since there are now 2 inputs, it would be "1. Hello\n2. How are you\n".

# Part 2
