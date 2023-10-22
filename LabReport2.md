# Lab Report 2
# Part 1
1. 
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/b3c16f44-5f31-483d-9e0d-5d9f5b3368c8)

2. 

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/6fce9765-5576-473d-9501-458eee01f6d1)
The methods that are being called are the handleRequest() method in the Handler class and the start() method in the Server.java file to create the server. The relavent arguments to the handleRequest() method is the URI url. Initially, the value of URI url is `http://localhost:4000/`; ArrayList inputs is a blank ArrayList; and String result has a blank string. After the request, the URI url gets repopulated with `http://localhost:4000/add-message?s=Hello` and the array String[] parameters gets populated with 2 values, the url `http://localhost:4000/add-message?s` as a String and the String inputted after `/add-message?s=` (in this case "Hello"). The fields that change afterwards is the ArrayList inputs, which adds the String "Hello", and the String result, and since there was only one input, it would be "1. Hello\n".

3. 

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/e70d9fd0-f145-421a-bb9b-6626a057b89a)
The methods that are being called are the handleRequest() method in the Handler class. The relavent arguments to the handleRequest() method is the URI url. Initially, the value of the URI url is `http://localhost:4000/add-message?s=Hello`; ArrayList inputs is an ArrayList with only one value, "Hello" at index 0; and String result would be already populated with "1. Hello\n". After the request, the URI url gets repopulated with `http://localhost:4000/add-message?s=How are you` and the array String[] parameters gets populated with 2 values, the url `http://localhost:4000/add-message?s` as a String, and the String inputted after `/add-message?s=` (in this case "How are you"). The fields that change after this request is the ArrayList inputs, which adds the String "How are you" (this makes the size of the ArrayList 2), and the String result, and since there are now 2 inputs, it would be "1. Hello\n2. How are you\n".

# Part 2
1. 

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/33dd2693-307c-4811-8ea6-f368ccc6c6c5)

The path is `\Users\mfbie\.ssh\id_rsa`.

2. 

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/d630a8ef-61d7-4cb4-b1d5-68efff01c9b8)

The path is `/home/linux/ieng6/cs15lfa23/cs15lfa23ad/.ssh/authorized_keys`

3. 

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/4fd4b7f1-5c47-485b-9e30-dab26d1793c0)

# Part 3
Most of what I learned in the past 2 labs were how easy it was to create a server or connect virtually to a different computer. Before, I thought it was this complicated and daunting tast, needing external software or deep understanding of HTML to create a server, but through the labs, I've learned that you can easily create one just by writing a couple correct java files and running them. Although they won't be the prettiest servers, this groundwork will be helpful in making more complicated ones in the future. On the other hand, for remote access, I was surprised that all you needed was the terminal, one command, and the computer you wanted to connect to. As before, I thought that you needed external software, since the other, seemingly more common, ways to connect virtually via a VPN or to my Mom's work computer always used to use external software. Therefore, this makes me think that a lot of the things that seem extremely complicated in Computer Science might not be as hard as they seem, while many other tasks that may seem simple might be significantly harder than they might seem.
