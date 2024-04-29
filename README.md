# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
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
## OUTPUT:
## CLIENT: 
![Screenshot 2024-04-29 081436](https://github.com/gayumee/3b_CHAT_USING_TCP_SOCKETS/assets/149037327/21d133ba-8d75-4c56-8163-23685e4b8d12)

## SERVER:
![Screenshot 2024-04-29 081509](https://github.com/gayumee/3b_CHAT_USING_TCP_SOCKETS/assets/149037327/5f71dc70-6d25-41f3-a8a8-b358f58daac8)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
