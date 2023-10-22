Lab Report 2
============
_Enrique Aranda_

__Part 1:__
The code for StringServer.java: 
![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/37708b63-b347-4151-b86f-ca588478fdc3)
![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/5a1d9302-d114-4251-a123-04393f88d485)

Examples of `/add-message` running: 
1. ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/326f2e53-23ca-4aaa-929c-3e923ef52c77)
   
2. ![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/e9cef560-6d0d-49f4-894c-b08930d00465)

The methods called are the main method in the `StringServer` class and the handleRequest method in the `Handler` class.
The relevant argument for the main method is the Port number because if the input is not within the specific range, the method will throw out an error. The relevant argument for the handleRequest method is the `/add-message?s=(input)` because it prints out the argument that the user manually types in.
The main value that changes is the num integer because it represents the line number of the web server and every new statement that the user types, the line number will increase by 1.

---
__Part 2:__
The path to the private key for my SSH key for logging into ieng6 is: /c/Users/enriq/id_rsa.pub

![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/3c620aaa-f971-49a7-91b2-0516cd26e86f)

The path to the public key forr my SSH key for logging into ieng6 is: /home/linux/ieng6/cs15lfa23/cs15lfa23os/authorized_keys
![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/ccf19b1a-0cda-4088-98a5-c3d24fcaf3f3)



Terminal interaction where I log into ieng6 without being asked for a password:
![image](https://github.com/earanda4/cse-15l-lab-report/assets/130427635/9a5c7d48-74e8-45e8-9056-74385b6f7140)

---
__Part 3:__
