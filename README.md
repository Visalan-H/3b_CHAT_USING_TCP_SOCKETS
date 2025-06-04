# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## Program:

#### Developed By: Visalan H
#### Register Number: 212223240183

### Server:

```
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
```

### Client:

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("Client > ")
s.send(msg.encode())
print("Server > ",s.recv(1024).decode())
```

## Output:

### Server:

![image](https://github.com/user-attachments/assets/1e9e0b61-155c-406b-aa6f-cce6c99e300a)

### Client:

![image](https://github.com/user-attachments/assets/deb8ff9c-905a-44c7-8ae2-365685372e48)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
