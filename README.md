# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT
### Client:
![Screenshot 2024-04-03 160256](https://github.com/POZHILANVD/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870498/28962c81-80c6-4593-97bd-06d4c552a507)
### Server:
![Screenshot 2024-04-03 160241](https://github.com/POZHILANVD/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870498/6e6d2971-aa3d-4bf5-ae4f-94fadcf02207)
## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
