# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name: HASMITHA V NANCY
## Reg No: 212224040111
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
client.py
~~~
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
~~~
server.py
~~~
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
~~~
## OUPUT
![Screenshot 2025-05-13 220352](https://github.com/user-attachments/assets/0f05c5ea-8eed-494e-985c-081b9d7c2521)

![image](https://github.com/user-attachments/assets/ecab1878-2c67-404c-8cfc-ffe7898a2510)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
