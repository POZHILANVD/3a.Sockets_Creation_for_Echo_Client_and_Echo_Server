## 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
### ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server .
4. Send and receive the message using the send function in socket.
## PROGRAM
#### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
#### Server
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
### OUPUT
#### Client:
![Screenshot 2024-04-03 160256](https://github.com/POZHILANVD/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870498/4d7eb12c-838f-4e3d-ae89-1d11174b01a3)
#### Server:
![Screenshot 2024-04-03 160241](https://github.com/POZHILANVD/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870498/a015aee4-1001-4732-9e0c-6fddb768fe5d)
### RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
